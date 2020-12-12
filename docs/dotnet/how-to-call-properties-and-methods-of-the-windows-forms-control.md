---
description: Дополнительные сведения см. в статье как вызвать свойства и методы элемента управления Windows Forms
title: Практическое руководство. Вызов свойств и методов элемента управления Windows Forms
ms.custom: get-started-article
ms.date: 11/04/2016
helpviewer_keywords:
- method calls, Windows Forms
- calling methods, Windows Forms control
- calling properties, Windows Forms control
- Windows Forms controls [C++], methods
- calling properties
- Windows Forms controls [C++], properties
ms.assetid: 6e647d8a-fdaa-4aa1-b3fe-04f15cff8eb3
ms.openlocfilehash: a797084a28eefec27699814a09c8521da7460bc7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97268409"
---
# <a name="how-to-call-properties-and-methods-of-the-windows-forms-control"></a>Практическое руководство. Вызов свойств и методов элемента управления Windows Forms

Поскольку [квинформсвиев::](../mfc/reference/cwinformsview-class.md#getcontrol) онинитиалупдате возвращает указатель на, <xref:System.Windows.Forms.Control?displayProperty=fullName> и не является указателем на `WindowsControlLibrary1::UserControl1` , рекомендуется добавить член типа пользовательского элемента управления и инициализировать его в [IView::](../mfc/reference/iview-interface.md#oninitialupdate). Теперь можно вызывать методы и свойства с помощью `m_ViewControl` .

В этом разделе предполагается, что вы уже выполнили [действия по созданию пользовательского элемента управления и узла в диалоговом окне](../dotnet/how-to-create-the-user-control-and-host-in-a-dialog-box.md) , а [также о том, как создать пользовательский элемент управления и представление узла MDI](../dotnet/how-to-create-the-user-control-and-host-mdi-view.md).

### <a name="to-create-the-mfc-host-application"></a>Создание ведущего приложения MFC

1. Откройте приложение MFC, созданное в окне [как создать пользовательский элемент управления и представление узла MDI](../dotnet/how-to-create-the-user-control-and-host-mdi-view.md).

1. Добавьте следующую строку в раздел public Overrides `CMFC02View` объявления класса в MFC02View. h.

   `gcroot<WindowsFormsControlLibrary1::UserControl1 ^> m_ViewControl;`

1. Добавьте переопределение для Онинитиалупдате.

   Отображение окна **Свойства** (F4). В **представление классов** (Ctrl + Shift + C) выберите класс CMFC02View. В окне **Свойства** выберите значок для переопределений. Сколл список до Онинитиалупдате. Щелкните раскрывающийся список и выберите \<Add> . В MFC02View. cpp. Убедитесь, что тело функции Онинитиалупдате имеет следующий вид:

    ```
    CWinFormsView::OnInitialUpdate();
    m_ViewControl = safe_cast<WindowsFormsControlLibrary1::UserControl1 ^>(this->GetControl());
    m_ViewControl->textBox1->Text = gcnew System::String("hi");
    ```

1. Постройте и запустите проект.

   В меню **Сборка** выберите **Собрать решение**.

   В меню **Отладка** выберите команду **Запуск без отладки**.

   Обратите внимание, что текстовое поле теперь инициализировано.

## <a name="see-also"></a>См. также раздел

[Размещение пользовательского элемента управления формы Windows Forms в качестве представления MFC](../dotnet/hosting-a-windows-forms-user-control-as-an-mfc-view.md)
