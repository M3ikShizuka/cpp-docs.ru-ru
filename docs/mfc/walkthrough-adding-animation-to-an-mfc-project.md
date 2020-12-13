---
description: Дополнительные сведения см. в разделе Пошаговое руководство. Добавление анимации в проект MFC
title: Пошаговое руководство. Добавление анимации в проект MFC
ms.date: 04/25/2019
helpviewer_keywords:
- animation [MFC]
- MFC, animation
ms.assetid: 004f832c-9fd5-4f88-9ca9-ae65dececdc2
ms.openlocfilehash: ef6d6fc8e17c8e6dc4c6f0f4e8d7407f2690927f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97143121"
---
# <a name="walkthrough-adding-animation-to-an-mfc-project"></a>Пошаговое руководство. Добавление анимации в проект MFC

В этом пошаговом руководстве объясняется, как добавить базовый анимированный объект в проект Visual C++, библиотека Microsoft Foundation Class (MFC).

В этом пошаговом руководстве показано, как выполнить следующие задачи.

- Создайте приложение MFC.

- Добавьте меню, а затем добавьте команды для запуска и завершения анимации.

- Создайте обработчики для команд Start и останавливают.

- Добавьте анимированный объект в проект.

- Центрирование анимированного объекта в окне.

- Проверьте результаты.

[!INCLUDE[note_settings_general](../mfc/includes/note_settings_general_md.md)]

## <a name="prerequisites"></a>Предварительные требования

Для выполнения инструкций этого пошагового руководства необходимо иметь Visual Studio.

### <a name="to-create-an-mfc-application"></a>Создание приложения MFC

1. Используйте **Мастер приложений MFC** для создания приложения MFC. Инструкции по открытию мастера для вашей версии Visual Studio см. в разделе [Пошаговое руководство. Использование новых элементов управления оболочки MFC](walkthrough-using-the-new-mfc-shell-controls.md) .

1. В поле **имя** введите *мфканиматионвалксраугх*. Нажмите кнопку **ОК**.

1. В диалоговом окне **Мастер приложений MFC** убедитесь, что для параметра **Тип приложения** выбрано значение **несколько документов**, **проект** имеет значение **Visual Studio** и выбран параметр **Поддержка архитектуры документов/представлений** . Нажмите кнопку **Готово**.

### <a name="to-add-a-menu-and-then-add-commands-to-start-and-stop-an-animation"></a>Добавление меню и Добавление команд для запуска и завершения анимации

1. В меню **вид** наведите указатель на пункт **другие окна** и выберите пункт **представление ресурсов**.

1. В **представление ресурсов** перейдите в папку **меню** и откройте ее. Дважды щелкните ресурс **IDR_MFCAnimationWalkthroughTYPE** , чтобы открыть его для изменения.

1. В строке меню в поле **тип** введите *&ниматион* , чтобы создать меню анимации.

1. В разделе **анимация** в поле **тип** введите *начать &вперед* , чтобы создать команду начать вперед.

1. В разделе **Начало вперед** в поле **тип** введите *Start &назад*.

1. В разделе **начать назад** в поле **тип** введите *S&Top* , чтобы создать команду "прерывать".

1. Сохраните Мфканиматионвалксраугх. RC и закройте его.

1. В **Обозреватель решений** дважды щелкните маинфрм. cpp, чтобы открыть его для изменения. В `CMainFrame::OnCreate` методе нахождение раздела, который содержит несколько вызовов `lstBasicCommands.AddTail` . Сразу после этого раздела добавьте следующий код.

    ```cpp
    lstBasicCommands.AddTail(ID_ANIMATION_STARTFORWARD);
    lstBasicCommands.AddTail(ID_ANIMATION_STARTBACKWARD);
    lstBasicCommands.AddTail(ID_ANIMATION_STOP);
    ```

1. Сохраните файл и закройте его.

### <a name="to-create-handlers-for-the-start-and-stop-commands"></a>Создание обработчиков для команд Start и останавливают

1. В меню **проект** выберите пункт **мастер классов**.

1. В **мастере классов MFC** в разделе **имя класса** выберите **кмфканиматионвалксраугхвиев**.

1. На вкладке **команды** в поле **идентификаторы объектов** выберите **ID_ANIMATION_STARTFORWARD**, а затем в поле **сообщения** выберите **команду**. Нажмите кнопку **Добавить обработчик**.

1. В диалоговом окне **Добавление функции члена** нажмите кнопку **ОК**.

1. В поле **идентификаторы объектов** выберите **ID_ANIMATION_STARTBACKWARD**, а затем в поле **сообщения** выберите **команду**. Нажмите кнопку **Добавить обработчик**.

1. В диалоговом окне **Добавление функции члена** нажмите кнопку **ОК**.

1. В поле **идентификаторы объектов** выберите **ID_ANIMATION_STOP**, а затем в поле **сообщения** выберите **команду**. Нажмите кнопку **Добавить обработчик** , а затем нажмите кнопку **ОК**.

1. В диалоговом окне **Добавление функции члена** нажмите кнопку **ОК**.

1. В **мастере классов MFC** нажмите кнопку **ОК**.

1. Сохраните Мфканиматионвалксраугхвиев. cpp, Открытый в редакторе, но не закрывайте его.

### <a name="to-add-an-animated-object-to-the-project"></a>Добавление анимированного объекта в проект

1. В **Обозреватель решений** дважды щелкните мфканиматионвалксраугхвиев. h, чтобы открыть его для изменения. Непосредственно перед определением `CMFCAnimationWalkthroughView` класса добавьте следующий код, чтобы создать пользовательский контроллер анимации, который будет выполнять конфликты планирования с объектом анимации.

    ```cpp
    class CCustomAnimationController : public CAnimationController
    {
    public:
        CCustomAnimationController()
        {
        }

        virtual BOOL OnHasPriorityTrim(CAnimationGroup* pGroupScheduled,
            CAnimationGroup* pGroupNew,
            UI_ANIMATION_PRIORITY_EFFECT priorityEffect)
        {
            return TRUE;
        }
    };
    ```

1. В конце `CMFCAnimationWalkthroughView` класса добавьте следующий код.

    ```cpp
    CCustomAnimationController m_animationController;
    CAnimationColor m_animationColor;
    CAnimationRect m_animationRect;
    ```

1. После `DECLARE_MESSAGE_MAP()` строки добавьте следующий код.

    ```cpp
    void Animate(BOOL bDirection);
    ```

1. Сохраните файл и закройте его.

1. В Мфканиматионвалксраугхвиев. cpp в начале файла после `#include` операторов, но перед любыми методами класса добавьте следующий код.

    ```cpp
    static int nAnimationGroup = 0;
    static int nInfoAreaHeight = 40;
    ```

1. В конце конструктора для `CMFCAnimationWalkthroughView` добавьте следующий код.

    ```cpp
    m_animationController.EnableAnimationTimerEventHandler();
    m_animationController.EnablePriorityComparisonHandler(UI_ANIMATION_PHT_TRIM);
    m_animationColor = RGB(255, 255, 255);
    m_animationRect = CRect(0, 0, 0, 0);
    m_animationColor.SetID(-1, nAnimationGroup);
    m_animationRect.SetID(-1, nAnimationGroup);
    m_animationController.AddAnimationObject(&m_animationColor);
    m_animationController.AddAnimationObject(&m_animationRect);
    ```

1. Найдите `CAnimationWalthroughView::PreCreateWindow` метод и замените его следующим кодом.

    ```cpp
    BOOL CMFCAnimationWalkthroughView::PreCreateWindow(CREATESTRUCT& cs)
    {
        // TODO: Modify the Window class or styles here by modifying
        //       the CREATESTRUCT cs
        m_animationController.SetRelatedWnd(this);

        return CView::PreCreateWindow(cs);
    }
    ```

1. Найдите `CAnimationWalkthroughView::OnDraw` метод и замените его следующим кодом.

    ```cpp
    void CMFCAnimationWalkthroughView::OnDraw(CDC* pDC)
    {
        CMFCAnimationWalkthroughDoc* pDoc = GetDocument();
        ASSERT_VALID(pDoc);
        if (!pDoc)
            return;

        // TODO: add draw code for native data here
        CMemDC dcMem(*pDC, this);
        CDC& dc = dcMem.GetDC();
        CRect rect;
        GetClientRect(rect);

        dc.FillSolidRect(rect, GetSysColor(COLOR_WINDOW));

        CString strRGB;
        strRGB.Format(_T("Fill Color is: %d; %d; %d"),
            GetRValue(m_animationColor),
            GetGValue(m_animationColor),
            GetBValue(m_animationColor));

        dc.DrawText(strRGB, rect, DT_CENTER);
        rect.top += nInfoAreaHeight;

        CBrush br;
        br.CreateSolidBrush(m_animationColor);
        CBrush* pBrushOld = dc.SelectObject(&br);

        dc.Rectangle((CRect)m_animationRect);

        dc.SelectObject(pBrushOld);
    }
    ```

1. В конце файла добавьте следующий код.

    ```cpp
    void CMFCAnimationWalkthroughView::Animate(BOOL bDirection)
    {
        static UI_ANIMATION_SECONDS duration = 3;
        static DOUBLE dblSpeed = 35.;
        static BYTE nStartColor = 50;
        static BYTE nEndColor = 255;

        BYTE nRedColorFinal = bDirection ? nStartColor : nEndColor;
        BYTE nGreenColorFinal = bDirection ? nStartColor : nEndColor;
        BYTE nBlueColorFinal = bDirection ? nStartColor : nEndColor;

        CLinearTransition* pRedTransition =
            new CLinearTransition(duration, (DOUBLE)nRedColorFinal);

        CSmoothStopTransition* pGreenTransition =
            new CSmoothStopTransition(duration, (DOUBLE)nGreenColorFinal);

        CLinearTransitionFromSpeed* pBlueTransition =
            new CLinearTransitionFromSpeed(dblSpeed, (DOUBLE)nBlueColorFinal);

        m_animationColor.AddTransition(pRedTransition,
            pGreenTransition,
            pBlueTransition);

        CRect rectClient;
        GetClientRect(rectClient);

        rectClient.top += nInfoAreaHeight;

        int nLeftFinal = bDirection ? rectClient.left : rectClient.CenterPoint().x;
        int nTopFinal = bDirection ? rectClient.top : rectClient.CenterPoint().y;
        int nRightFinal = bDirection ? rectClient.right : rectClient.CenterPoint().x;
        int nBottomFinal = bDirection ? rectClient.bottom : rectClient.CenterPoint().y;

        CLinearTransition* pLeftTransition =
            new CLinearTransition(duration, nLeftFinal);

        CLinearTransition* pTopTransition =
            new CLinearTransition(duration, nTopFinal);

        CLinearTransition* pRightTransition =
            new CLinearTransition(duration, nRightFinal);

        CLinearTransition* pBottomTransition =
            new CLinearTransition(duration, nBottomFinal);

        m_animationRect.AddTransition(pLeftTransition,
            pTopTransition,
            pRightTransition,
            pBottomTransition);

        CBaseKeyFrame* pKeyframeStart =
            CAnimationController::GetKeyframeStoryboardStart();
        CKeyFrame* pKeyFrameEnd =
            m_animationController.CreateKeyframe(nAnimationGroup,
                pBlueTransition);

        pLeftTransition->SetKeyframes(pKeyframeStart, pKeyFrameEnd);
        pTopTransition->SetKeyframes(pKeyframeStart, pKeyFrameEnd);
        pRightTransition->SetKeyframes(pKeyframeStart, pKeyFrameEnd);
        pBottomTransition->SetKeyframes(pKeyframeStart, pKeyFrameEnd);

        m_animationController.AnimateGroup(nAnimationGroup);
    }
    ```

1. В меню **проект** выберите пункт **мастер классов**.

1. В **мастере классов MFC** в разделе **имя класса** выберите **кмфканиматионвалксраугхвиев**.

1. На вкладке **сообщения** в поле **сообщения** выберите **WM_ERASEBKGND**, щелкните **Добавить обработчик**, а затем нажмите кнопку **ОК**.

1. В Мфканиматионвалксраугхвиев. cpp Замените реализацию `OnEraseBkgnd` следующим кодом, чтобы уменьшить мерцание анимированного объекта при его перерисовке.

    ```cpp
    BOOL CMFCAnimationWalkthroughView::OnEraseBkgnd(CDC* /*pDC*/)
    {
        return TRUE;
    }
    ```

1. Замените реализации `CMFCAnimationWalkthroughView::OnAnimationStartforward` , `CMFCAnimationWalkthroughView::OnAnimationStartbackward` и `CMFCAnimationWalkthroughView::OnAnimationStop` следующим кодом.

    ```cpp
    void CMFCAnimationWalkthroughView::OnAnimationStartforward()
    {
        Animate(TRUE);
    }

    void CMFCAnimationWalkthroughView::OnAnimationStartbackward()
    {
        Animate(FALSE);
    }

    void CMFCAnimationWalkthroughView::OnAnimationStop()
    {
        IUIAnimationManager* pManager = m_animationController.GetUIAnimationManager();
        if (pManager != NULL)
        {
            pManager->AbandonAllStoryboards();

        }
    }
    ```

1. Сохраните файл и закройте его.

### <a name="to-center-the-animated-object-in-the-window"></a>Центрирование анимированного объекта в окне

1. В **Обозреватель решений** дважды щелкните мфканиматионвалксраугхвиев. h, чтобы открыть его для изменения. В конце `CMFCAnimationWalkthroughView` класса сразу после определения `m_animationRect` добавьте следующий код.

    ```cpp
    BOOL m_bCurrentDirection;
    ```

1. Сохраните файл и закройте его.

1. В меню **проект** выберите пункт **мастер классов**.

1. В **мастере классов MFC** в разделе **имя класса** выберите **кмфканиматионвалксраугхвиев**.

1. На вкладке **сообщения** в поле **сообщения** выберите **WM_SIZE**, щелкните **Добавить обработчик**, а затем нажмите кнопку **ОК**.

1. В Мфканиматионвалксраугхвиев. cpp замените код на `CMFCAnimationWalkthroughView::OnSize` следующий код.

    ```cpp
    void CMFCAnimationWalkthroughView::OnSize(UINT nType, int cx, int cy)
    {
        CView::OnSize(nType, cx, cy);
        CRect rect;
        GetClientRect(rect);

        rect.top += nInfoAreaHeight;

        CRect rectAnim = m_animationRect;
        m_animationRect = CRect(CPoint(rect.CenterPoint().x - rectAnim.Width() / 2,
        rect.CenterPoint().y - rectAnim.Height() / 2),
        rectAnim.Size());

        if (m_animationController.IsAnimationInProgress())
        {
            Animate(m_bCurrentDirection);
        }
    }
    ```

1. В начале конструктора для `CMFCAnimationWalkthroughView` добавьте следующий код.

    ```cpp
    m_bCurrentDirection = TRUE;
    ```

1. В начале `CMFCAnimationWalkthroughView::Animate` метода добавьте следующий код.

    ```cpp
    m_bCurrentDirection = bDirection;
    ```

1. Сохраните файл и закройте его.

### <a name="to-verify-the-results"></a>Проверка результатов

1. Создайте и запустите приложение. В меню **анимация** выберите команду **начать вперед**. Должен отобразиться прямоугольник, а затем заполнить центральную область. При нажатии кнопки **начать назад** анимация должна быть обратной, а при нажатии кнопки " **прерывать**" она должна быть прервана. Цвет заливки прямоугольника должен изменяться по мере продвижения анимации, а текущий цвет должен отображаться в верхней части окна анимации.

## <a name="see-also"></a>См. также раздел

[Пошаговые руководства](../mfc/walkthroughs-mfc.md)
