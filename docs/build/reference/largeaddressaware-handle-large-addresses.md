---
description: Дополнительные сведения о:/LARGEADDRESSAWARE (работа с большими адресами)
title: /LARGEADDRESSAWARE (Обрабатывать большие адреса)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.LargeAddressAware
- /largeaddressaware
helpviewer_keywords:
- LARGEADDRESSAWARE linker option
- -LARGEADDRESSAWARE linker option
- /LARGEADDRESSAWARE linker option
ms.assetid: a29756c8-e893-47a9-9750-1f0d25359385
ms.openlocfilehash: 72b2ba20b2ea2b91ecd234497c433bcdd9e9ee42
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97199575"
---
# <a name="largeaddressaware-handle-large-addresses"></a>/LARGEADDRESSAWARE (Обрабатывать большие адреса)

```
/LARGEADDRESSAWARE[:NO]
```

## <a name="remarks"></a>Комментарии

Параметр/LARGEADDRESSAWARE сообщает компоновщику, что приложение может управлять адресами, превышающими 2 гигабайта. В 64-разрядных компиляторах этот параметр включен по умолчанию. В 32-разрядных компиляторах/LARGEADDRESSAWARE: NO включено, если/LARGEADDRESSAWARE не указан в строке компоновщика.

Если приложение было связано с/LARGEADDRESSAWARE, в подмассиве [dumpbin будет](headers.md) отображаться информация об этом результате.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **системы** .

1. Измените свойство **включить большие адреса** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.LargeAddressAware%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
