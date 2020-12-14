---
description: Дополнительные сведения см. в статье как добавить маршрутизацию команд в элемент управления Windows Forms
title: Практическое руководство. Добавление маршрутизации команд в элемент управления Windows Forms
ms.custom: get-started-article
ms.date: 11/04/2016
helpviewer_keywords:
- command routing [C++], adding to Windows Forms controls
- Windows Forms controls [C++], command routing
ms.assetid: bf138ece-b463-442a-b0a0-de7063a760c0
ms.openlocfilehash: b46087d7df3da5f402432731db4b994b257a385b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335419"
---
# <a name="how-to-add-command-routing-to-the-windows-forms-control"></a>Практическое руководство. Добавление маршрутизации команд в элемент управления Windows Forms

[Квинформсвиев](../mfc/reference/cwinformsview-class.md) маршрутизирует команды и сообщения пользовательского интерфейса команды обновления в пользовательский элемент управления, чтобы разрешить ему обработку команд MFC (например, элементы меню "фрейм" и кнопки панели инструментов).

Пользовательский элемент управления использует [ICommandTarget:: Initialize](../mfc/reference/icommandtarget-interface.md#initialize) для хранения ссылки на исходный объект команды в `m_CmdSrc` , как показано в следующем примере. Чтобы использовать `ICommandTarget` , необходимо добавить ссылку на mfcmifc80.dll.

`CWinFormsView` обрабатывает несколько распространенных уведомлений представления MFC, пересылая их в управляемый пользовательский элемент управления. Эти уведомления включают методы [онинитиалупдате](../mfc/reference/iview-interface.md#oninitialupdate), [OnUpdate](../mfc/reference/iview-interface.md#onupdate) и [онактиватевиев](../mfc/reference/iview-interface.md#onactivateview) .

В этом разделе предполагается, что вы уже выполнили [действия по созданию пользовательского элемента управления и узла в диалоговом окне](../dotnet/how-to-create-the-user-control-and-host-in-a-dialog-box.md) , а [также о том, как создать пользовательский элемент управления и представление узла MDI](../dotnet/how-to-create-the-user-control-and-host-mdi-view.md).

### <a name="to-create-the-mfc-host-application"></a>Создание ведущего приложения MFC

1. Откройте библиотеку элементов управления Windows Forms, созданную в [процедуре Создание пользовательского элемента управления и узла в диалоговом окне](../dotnet/how-to-create-the-user-control-and-host-in-a-dialog-box.md).

1. Добавьте ссылку на mfcmifc80.dll, которую можно сделать, щелкнув правой кнопкой мыши узел проекта в **Обозреватель решений**, выбрав **Добавить**, **ссылку**, а затем перейду к Microsoft Visual Studio 10.0 \ вк\атлмфк\либ.

1. Откройте UserControl1.Designer.cs и добавьте следующую инструкцию using:

    ```
    using Microsoft.VisualC.MFC;
    ```

1. Кроме того, в UserControl1.Designer.cs измените эту строку:

    ```
    partial class UserControl1
    ```

   на такой:

    ```
    partial class UserControl1 : System.Windows.Forms.UserControl, ICommandTarget
    ```

1. Добавьте его в качестве первой строки определения класса для `UserControl1` :

    ```
    private ICommandSource m_CmdSrc;
    ```

1. Добавьте следующие определения методов в `UserControl1` (мы создадим идентификатор элемента управления MFC на следующем шаге):

    ```
    public void Initialize (ICommandSource cmdSrc)
    {
       m_CmdSrc = cmdSrc;
       // need ID of control in MFC dialog and callback function
       m_CmdSrc.AddCommandHandler(32771, new CommandHandler (singleMenuHandler));
    }

    private void singleMenuHandler (uint cmdUI)
    {
       // User command handler code
       System.Windows.Forms.MessageBox.Show("Custom menu option was clicked.");
    }
    ```

1. Откройте приложение MFC, созданное в окне [как создать пользовательский элемент управления и представление узла MDI](../dotnet/how-to-create-the-user-control-and-host-mdi-view.md).

1. Добавьте параметр меню, который будет вызывать `singleMenuHandler` .

   Перейдите в **представление ресурсов** (Ctrl + Shift + E), разверните папку **меню** , а затем дважды щелкните **IDR_MFC02TYPE**. Откроется редактор меню.

   Добавьте пункт меню в нижней части меню **вид** . Обратите внимание на идентификатор пункта меню в окне **Свойства** . Сохраните файл.

   В **Обозреватель решений** откройте файл Resource. h, СКОПИРУЙТЕ значение идентификатора только что добавленного пункта меню и вставьте это значение в качестве первого параметра в `m_CmdSrc.AddCommandHandler` вызов в `Initialize` методе проекта C# ( `32771` при необходимости замените его).

1. Постройте и запустите проект.

   В меню **Сборка** выберите **Собрать решение**.

   В меню **Отладка** выберите команду **Запуск без отладки**.

   Выберите добавленный пункт меню. Обратите внимание, что вызывается метод в библиотеке DLL.

## <a name="see-also"></a>См. также раздел

[Размещение пользовательского элемента управления формы Windows Forms в качестве представления MFC](../dotnet/hosting-a-windows-forms-user-control-as-an-mfc-view.md)<br/>
[Интерфейс ICommandSource](../mfc/reference/icommandsource-interface.md)<br/>
[Интерфейс ICommandTarget](../mfc/reference/icommandtarget-interface.md)
