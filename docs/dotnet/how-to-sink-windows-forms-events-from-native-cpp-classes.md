---
description: 'Дополнительные сведения о: как приемник Windows Forms события из собственных классов C++'
title: Практическое руководство. Получение событий Windows Forms из собственных классов C++
ms.custom: get-started-article
ms.date: 11/04/2016
helpviewer_keywords:
- event handling, managed/native interop
- event handling, sinking .NET in C++
- event handling, .NET/native interop
- event handling, Windows Forms in C++
ms.assetid: 6e30ddee-d058-4c8d-9956-2a43d86f19d5
ms.openlocfilehash: 223590849f114bfe02b030a0639f160b8fc1c321
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97286362"
---
# <a name="how-to-sink-windows-forms-events-from-native-c-classes"></a>Практическое руководство. Получение событий Windows Forms из собственных классов C++

Можно включить собственные классы C++ для получения обратных вызовов от управляемых событий, вызванных Windows Forms элементами управления или другими формами, с помощью формата схемы макросов MFC. События-приемники в представлениях и диалоговых окнах похожи на выполнение одной и той же задачи для элементов управления.

Для этого необходимо выполнить следующие действия.

- Присоедините `OnClick` обработчик событий к элементу управления с помощью [MAKE_DELEGATE](../mfc/reference/delegate-and-interface-maps.md#make_delegate).

- Создайте карту делегатов с помощью [BEGIN_DELEGATE_MAP](../mfc/reference/delegate-and-interface-maps.md#begin_delegate_map), [END_DELEGATE_MAP](../mfc/reference/delegate-and-interface-maps.md#end_delegate_map)и [EVENT_DELEGATE_ENTRY](../mfc/reference/delegate-and-interface-maps.md#event_delegate_entry).

В этом примере пройдется работа, выполненная в ходе [выполнения привязки данных DDX/DDV с Windows Forms](../dotnet/how-to-do-ddx-ddv-data-binding-with-windows-forms.md).

Теперь вы свяжете элемент управления MFC ( `m_MyControl` ) с управляемым делегатом обработчика событий, который вызывается `OnClick` для управляемого <xref:System.Windows.Forms.Control.Click> события.

### <a name="to-attach-the-onclick-event-handler"></a>Чтобы присоединить обработчик событий OnClick, сделайте следующее:

1. Добавьте следующий код в реализацию BOOL CMFC01Dlg:: Онинитдиалог:

    ```
    m_MyControl.GetControl()->button1->Click += MAKE_DELEGATE( System::EventHandler, OnClick );
    ```

1. Добавьте следующий код в общедоступный раздел в объявлении класса CMFC01Dlg: public CDialog.

    ```
    // delegate map
    BEGIN_DELEGATE_MAP( CMFC01Dlg )
    EVENT_DELEGATE_ENTRY( OnClick, System::Object^, System::EventArgs^ )
    END_DELEGATE_MAP()

    void OnClick( System::Object^ sender, System::EventArgs^ e );
    ```

1. Наконец, добавьте реализацию для `OnClick` в CMFC01Dlg. cpp:

    ```
    void CMFC01Dlg::OnClick(System::Object^ sender, System::EventArgs^ e)
    {
        AfxMessageBox(_T("Button clicked"));
    }
    ```

## <a name="see-also"></a>См. также раздел

[MAKE_DELEGATE](../mfc/reference/delegate-and-interface-maps.md#make_delegate)<br/>
[BEGIN_DELEGATE_MAP](../mfc/reference/delegate-and-interface-maps.md#begin_delegate_map)<br/>
[END_DELEGATE_MAP](../mfc/reference/delegate-and-interface-maps.md#end_delegate_map)<br/>
[EVENT_DELEGATE_ENTRY](../mfc/reference/delegate-and-interface-maps.md#event_delegate_entry)
