---
description: Дополнительные сведения см. в статье Использование пользовательского элемента управления формы Windows в MFC.
title: Использование пользовательского элемента управления формы Windows Form в MFC
ms.date: 01/08/2018
helpviewer_keywords:
- MFC [C++], Windows Forms support
- interoperability [C++], Windows Forms in MFC
- interoperability [C++], MFC
- interop [C++], Windows Forms in MFC
- interop [C++], MFC
- Windows Forms [C++], MFC support
ms.assetid: 63fb099b-1dff-469c-9e34-dab52e122fcd
ms.openlocfilehash: 61022d241faba1650d1a044ef6d3667febe34cde
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97319031"
---
# <a name="using-a-windows-form-user-control-in-mfc"></a>Использование пользовательского элемента управления формы Windows Form в MFC

С помощью классов поддержки MFC Windows Forms можно размещать элементы управления Windows Forms в приложениях MFC в виде элемента управления ActiveX в диалоговых окнах или представлениях MFC. Кроме того, Windows Forms формы могут размещаться в виде диалоговых окон MFC.

В следующих разделах описывается:

- Размещение элемента управления Windows Forms в диалоговом окне MFC.

- Размещение пользовательского элемента управления Windows Forms как представления MFC.

- Размещение Windows Forms формы в виде диалогового окна MFC.

> [!NOTE]
> Интеграция с MFC Windows Forms работает только в проектах, которые динамически связываются с MFC (проектами, в которых `_AFXDLL` определен).

> [!NOTE]
> При сборке приложения с помощью закрытой (измененной) копии библиотеки DLL Windows Forms интерфейсы MFC (mfcmifc80.dll) она не будет установлена в глобальном кэше сборок, если вы не замените ключ Майкрософт своим ключом поставщика. Дополнительные сведения о подписывании сборок см. в разделе [программирование со сборками](/dotnet/framework/app-domains/programming-with-assemblies) и [сборками со строгими именами (подписывание сборок) (C++/CLI)](../dotnet/strong-name-assemblies-assembly-signing-cpp-cli.md).

Если приложение MFC использует Windows Forms, необходимо повторно распространить mfcmifc80.dll с приложением. Дополнительные сведения см. [в разделе распространение библиотеки MFC](../windows/redistributing-the-mfc-library.md).

## <a name="in-this-section"></a>в этом разделе

[Размещение пользовательского элемента управления формы Windows Forms в диалоговом окне MFC](../dotnet/hosting-a-windows-form-user-control-in-an-mfc-dialog-box.md)

[Размещение пользовательского элемента управления формы Windows Forms в качестве представления MFC](../dotnet/hosting-a-windows-forms-user-control-as-an-mfc-view.md)

[Размещение пользовательского элемента управления формы Windows Forms в виде диалогового окна MFC](../dotnet/hosting-a-windows-form-user-control-as-an-mfc-dialog-box.md)

## <a name="reference"></a>Ссылка

[Класс Квинформсконтрол](../mfc/reference/cwinformscontrol-class.md)

[Класс Квинформсдиалог](../mfc/reference/cwinformsdialog-class.md)

[Класс Квинформсвиев](../mfc/reference/cwinformsview-class.md)

[Интерфейс ICommandSource](../mfc/reference/icommandsource-interface.md)

[Интерфейс ICommandTarget](../mfc/reference/icommandtarget-interface.md)

[Интерфейс Икоммандуи](../mfc/reference/icommandui-interface.md)

[Интерфейс IView](../mfc/reference/iview-interface.md)

[CommandHandler](../atl/commandhandler.md)

[DDX_ManagedControl](../mfc/reference/standard-dialog-data-exchange-routines.md#ddx_managedcontrol)

[UICheckState](../mfc/reference/uicheckstate-enumeration.md)

## <a name="related-sections"></a>Связанные разделы

[Windows Forms](/dotnet/framework/winforms/index)

[Элементы управления Windows Forms](/dotnet/framework/winforms/controls/index)

## <a name="see-also"></a>См. также раздел

[Элементы пользовательского интерфейса](../mfc/user-interface-elements-mfc.md)<br/>
[Представления форм](../mfc/form-views-mfc.md)
