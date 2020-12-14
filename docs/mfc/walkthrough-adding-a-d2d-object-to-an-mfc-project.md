---
description: Дополнительные сведения см. в разделе Пошаговое руководство. Добавление объекта D2D в проект MFC
title: Пошаговое руководство. Добавление объекта D2D в проект MFC
ms.date: 04/25/2019
helpviewer_keywords:
- MFC, D2D
- D2D [MFC]
ms.assetid: dda36c33-c231-4da6-a62f-72d69a12b6dd
ms.openlocfilehash: bbc59a943f6d8503370ddc8b7255275a6902b3c9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97344904"
---
# <a name="walkthrough-adding-a-d2d-object-to-an-mfc-project"></a>Пошаговое руководство. Добавление объекта D2D в проект MFC

В этом пошаговом руководстве объясняется, как добавить базовый объект Direct2D (D2D) в проект Visual C++, библиотека Microsoft Foundation Class (MFC), а затем построить проект в приложении, которое выводит «Hello, World!». на фоне градиента.

В этом пошаговом руководстве показано, как выполнить следующие задачи.

- Создайте приложение MFC.

- Создайте кисть с сплошным цветом и линейную градиентную кисть.

- Измените кисть градиента таким образом, чтобы она изменится соответствующим образом при изменении размера окна.

- Реализуйте обработчик рисования D2D.

- Проверьте результаты.

[!INCLUDE[note_settings_general](../mfc/includes/note_settings_general_md.md)]

## <a name="prerequisites"></a>Предварительные требования

Для выполнения этого пошагового руководства необходимо установить Visual Studio с рабочей нагрузкой **Разработка классических приложений на C++** и необязательный **Visual C++ MFC для компонентов x86 и x64** .

## <a name="to-create-an-mfc-application"></a>Создание приложения MFC

1. Используйте **Мастер приложений MFC** для создания приложения MFC. Инструкции по открытию мастера для вашей версии Visual Studio см. в разделе [Пошаговое руководство. Использование новых элементов управления оболочки MFC](walkthrough-using-the-new-mfc-shell-controls.md) .

1. В поле **имя** введите *MFCD2DWalkthrough*. Нажмите кнопку **ОК**.

1. В **мастере приложений MFC** нажмите кнопку **Готово** , не изменяя параметры.

## <a name="to-create-a-solid-color-brush-and-a-linear-gradient-brush"></a>Создание кисти с сплошным цветом и кисти линейного градиента

1. В **Обозреватель решений** в проекте **MFCD2DWalkthrough** в папке **файлы заголовков откройте файл** MFCD2DWalkthroughView. h. Добавьте следующий код в `CMFCD2DWalkthroughView` класс, чтобы создать три переменные данных:

   ```cpp
   CD2DTextFormat* m_pTextFormat;
   CD2DSolidColorBrush* m_pBlackBrush;
   CD2DLinearGradientBrush* m_pLinearGradientBrush;
   ```

   Сохраните файл и закройте его.

1. В папке **исходные файлы откройте файл** MFCD2DWalkthroughView. cpp. В конструкторе `CMFCD2DWalkthroughView` класса добавьте следующий код:

   ```cpp
   // Enable D2D support for this window:
   EnableD2DSupport();

   // Initialize D2D resources:
   m_pBlackBrush = new CD2DSolidColorBrush(
       GetRenderTarget(),
       D2D1::ColorF(D2D1::ColorF::Black));

   m_pTextFormat = new CD2DTextFormat(
       GetRenderTarget(),
       _T("Verdana"),
       50);

   m_pTextFormat->Get()->SetTextAlignment(
       DWRITE_TEXT_ALIGNMENT_CENTER);

   m_pTextFormat->Get()->SetParagraphAlignment(
       DWRITE_PARAGRAPH_ALIGNMENT_CENTER);

   D2D1_GRADIENT_STOP gradientStops[2];

   gradientStops[0].color =
       D2D1::ColorF(D2D1::ColorF::White);

   gradientStops[0].position = 0.f;
   gradientStops[1].color =
       D2D1::ColorF(D2D1::ColorF::Indigo);

   gradientStops[1].position = 1.f;

   m_pLinearGradientBrush = new CD2DLinearGradientBrush(
       GetRenderTarget(),
       gradientStops,
       ARRAYSIZE(gradientStops),
       D2D1::LinearGradientBrushProperties(
           D2D1::Point2F(0,0),
           D2D1::Point2F(0,0)));
   ```

   Сохраните файл и закройте его.

## <a name="to-modify-the-gradient-brush-so-that-it-will-change-appropriately-when-the-window-is-resized"></a>Изменение кисти градиента таким образом, чтобы она изменялась соответствующим образом при изменении размера окна

1. В меню **проект** выберите пункт **мастер классов**.

1. В **мастере классов MFC** в разделе **имя класса** выберите `CMFCD2DWalkthroughView` .

1. На вкладке **сообщения** в поле **сообщения** выберите `WM_SIZE` и нажмите кнопку **Добавить обработчик**. Это действие добавляет `OnSize` обработчик сообщений в `CMFCD2DWalkthroughView` класс.

1. В поле **существующие обработчики** выберите `OnSize` . Выберите **изменить код** , чтобы отобразить `CMFCD2DWalkthroughView::OnSize` метод. В конце метода добавьте следующий код.

   ```cpp
   m_pLinearGradientBrush->SetEndPoint(CPoint(cx, cy));
   ```

   Сохраните файл и закройте его.

## <a name="to-implement-a-d2d-drawing-handler"></a>Реализация обработчика рисования D2D

1. В меню **проект** выберите пункт **мастер классов**.

1. В **мастере классов MFC** в разделе **имя класса** выберите `CMFCD2DWalkthroughView` .

1. На вкладке **сообщения** выберите **Добавить настраиваемое сообщение**.

1. В диалоговом окне **Добавление настраиваемого сообщения** в окне **настраиваемое сообщение Windows** введите *AFX_WM_DRAW2D*. В поле **имя обработчика сообщений** введите *OnDraw2D*. Выберите параметр **зарегистрированное сообщение** и нажмите кнопку **ОК**. Это действие добавляет обработчик сообщений для AFX_WM_DRAW2D сообщения в `CMFCD2DWalkthroughView` класс.

1. В поле **существующие обработчики** выберите `OnDraw2D` . Выберите **изменить код** , чтобы отобразить `CMFCD2DWalkthroughView::OnDraw2D` метод. Используйте этот код для `CMFCD2DWalkthroughView::OnDrawD2D` метода:

   ```cpp
   afx_msg LRESULT CMFCD2DWalkthroughView::OnDraw2D(
       WPARAM wParam,
       LPARAM lParam)
   {
       CHwndRenderTarget* pRenderTarget = (CHwndRenderTarget*)lParam;
       ASSERT_VALID(pRenderTarget);

       CRect rect;
       GetClientRect(rect);

       pRenderTarget->FillRectangle(rect, m_pLinearGradientBrush);

       pRenderTarget->DrawText(
           _T("Hello, World!"),
           rect,
           m_pBlackBrush,
           m_pTextFormat);

       return TRUE;
   }
   ```

   Сохраните файл и закройте его.

## <a name="to-verify-the-results"></a>Проверка результатов

Создайте и запустите приложение. Он должен иметь прямоугольник градиента, который изменяется при изменении размера окна. "Hello World!" должен отображаться в центре прямоугольника.

## <a name="see-also"></a>См. также раздел

[Пошаговые руководства](../mfc/walkthroughs-mfc.md)
