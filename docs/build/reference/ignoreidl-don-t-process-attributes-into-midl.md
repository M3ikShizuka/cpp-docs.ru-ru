---
description: Дополнительные сведения о:/IGNOREIDL (Дон&#39;t обработка атрибутов в MIDL)
title: /IGNOREIDL (Дон&#39;t обрабатывать атрибуты в MIDL)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.IgnoreEmbeddedIDL
- /ignoreidl
helpviewer_keywords:
- IGNOREIDL linker option
- -IGNOREIDL linker option
- /IGNOREIDL linker option
ms.assetid: 29514098-6a1c-4317-af2f-1dc268972780
ms.openlocfilehash: c68b3ec2f9bd5607ef523667bcddc68b22d3c34c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97199822"
---
# <a name="ignoreidl-don39t-process-attributes-into-midl"></a>/IGNOREIDL (Дон&#39;t обрабатывать атрибуты в MIDL)

```
/IGNOREIDL
```

## <a name="remarks"></a>Комментарии

Параметр/IGNOREIDL указывает, что любые [атрибуты IDL](../../windows/attributes/idl-attributes.md) в исходном коде не должны обрабатываться в IDL-файле.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Щелкните страницу свойств **встроенного IDL** .

1. Измените параметр **игнорировать внедренное свойство IDL** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.IgnoreEmbeddedIDL%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)<br/>
[/IDLOUT (имя выходных файлов MIDL)](idlout-name-midl-output-files.md)<br/>
[/TLBOUT (имя. TLB-файл)](tlbout-name-dot-tlb-file.md)<br/>
[/MIDL (указание параметров командной строки MIDL)](midl-specify-midl-command-line-options.md)<br/>
[Сборка атрибутированной программы](../../windows/attributes/cpp-attributes-com-net.md)
