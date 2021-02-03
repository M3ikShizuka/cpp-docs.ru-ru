---
description: 'Дополнительные сведения: размещение пользовательского элемента управления Windows Forms как представления MFC'
title: Размещение пользовательского элемента управления формы Windows Forms в качестве представления MFC
ms.date: 11/04/2016
helpviewer_keywords:
- MFC [C++], Windows Forms support
- Windows Forms controls [C++], hosting as an MFC view
- hosting Windows Forms control [C++]
ms.assetid: 43c02ab4-1366-434c-a980-0b19326d6ea0
ms.openlocfilehash: 2db44bd4d85150b0a2b8fc1f2206af765770e9ed
ms.sourcegitcommit: 3987d9c39f5a5b4824303a48a6215984ce8949e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/02/2021
ms.locfileid: "99478148"
---
# <a name="hosting-a-windows-forms-user-control-as-an-mfc-view"></a>Размещение пользовательского элемента управления формы Windows Forms в качестве представления MFC

MFC использует класс Квинформсвиев для размещения пользовательского элемента управления Windows Forms в представлении MFC. Представления Windows Forms MFC — это элементы управления ActiveX. Пользовательский элемент управления размещается как дочерний для собственного представления и занимает всю клиентскую область собственного представления.

Конечный результат напоминает модель, используемую [классом CFormView](../mfc/reference/cformview-class.md). Это позволяет использовать преимущества конструктора Windows Forms и среды выполнения для создания расширенных представлений на основе форм.

Так как представления MFC Windows Forms являются элементами управления ActiveX, они не имеют таких же, `hwnd` как представления MFC. Они также не могут быть переданы в виде указателя на представление [CView](../mfc/reference/cview-class.md) . Как правило, используйте платформа .NET Framework методы для работы с представлениями Windows Forms и не зависеть от Win32.

Пример приложения, в котором показаны Windows Forms, используемые в MFC, см. в разделе [Интеграция MFC и Windows Forms](https://download.cnet.com/MFC-and-WinForms-Integration/3000-2383_4-75453644.html).

## <a name="in-this-section"></a>В этом разделе

[Как создать пользовательский элемент управления и представление узла MDI](../dotnet/how-to-create-the-user-control-and-host-mdi-view.md)

[Как добавить маршрутизацию команд в элемент управления Windows Forms](../dotnet/how-to-add-command-routing-to-the-windows-forms-control.md)

[Как вызвать свойства и методы элемента управления Windows Forms](../dotnet/how-to-call-properties-and-methods-of-the-windows-forms-control.md)

## <a name="see-also"></a>См. также раздел

[Использование пользовательского элемента управления формы Windows Forms в MFC](../dotnet/using-a-windows-form-user-control-in-mfc.md)<br/>
[Практическое руководство. Создание составных элементов управления](/dotnet/framework/winforms/controls/how-to-author-composite-controls)
