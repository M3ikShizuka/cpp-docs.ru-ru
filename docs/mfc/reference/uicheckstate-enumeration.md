---
description: Дополнительные сведения о перечислении Уичеккстате
title: Перечисление UICheckState
ms.date: 04/03/2017
f1_keywords:
- afxwinforms/uicheckstate
helpviewer_keywords:
- uicheckstate enumeration [MFC]
ms.assetid: 2ac0098c-20e7-410c-9685-5ead5cb02b63
ms.openlocfilehash: 8c6f250dd6f6646d22aac0fa819b73537ee0f443
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97218645"
---
# <a name="uicheckstate-enumeration"></a>Перечисление UICheckState

Описывает состояние проверки элемента пользовательского интерфейса для команды.

### <a name="syntax"></a>Синтаксис

```
public enum class
{
   [DefaultValue(typeid<Microsoft::VisualC::MFC::UICheckState>, "Checked")]
   Unchecked,
   Checked,
   Indeterminate
};
```

### <a name="remarks"></a>Remarks

[Икоммандуи:: Check](icommandui-interface.md#check) использует эти значения для описания состояния элемента пользовательского интерфейса.
Дополнительные сведения об использовании Windows Forms см. в разделе [Использование пользовательского элемента управления формы Windows в MFC](../../dotnet/using-a-windows-form-user-control-in-mfc.md).

### <a name="requirements"></a>Требования

**Заголовок:** афксвинформс. h (определяется в atlmfc\lib\mfcmifc80.dll сборки)
