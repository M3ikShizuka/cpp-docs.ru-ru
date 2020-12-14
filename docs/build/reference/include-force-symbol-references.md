---
description: Дополнительные сведения о:/INCLUDE (Принудительная ссылка на символы)
title: /INCLUDE (принудительные ссылки на символы)
ms.date: 11/04/2016
f1_keywords:
- /include
- VC.Project.VCLinkerTool.ForceSymbolReferences
helpviewer_keywords:
- INCLUDE linker option
- force symbol references linker option
- symbol references linker force
- /INCLUDE linker option
- symbols, add to symbol table
- -INCLUDE linker option
ms.assetid: 4a039677-360a-480f-bd0b-448e239b449c
ms.openlocfilehash: 4938f5e92f91718f522df103303e6382005d463c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97191307"
---
# <a name="include-force-symbol-references"></a>/INCLUDE (принудительные ссылки на символы)

```
/INCLUDE:symbol
```

## <a name="parameters"></a>Параметры

*знак*<br/>
Задает символ, добавляемый в таблицу символов.

## <a name="remarks"></a>Комментарии

Параметр/INCLUDE указывает компоновщику добавить указанный символ в таблицу символов.

Чтобы указать несколько символов, введите запятую (,), точку с запятой (;) или пробел между именами символов. В командной строке укажите/INCLUDE: `symbol` один раз для каждого символа.

Компоновщик разрешается `symbol` путем добавления объекта, содержащего определение символа, в программу. Эта функция полезна для включения объекта библиотеки, который в противном случае не будет связан с программой.

Указание символа с этим параметром переопределяет удаление этого символа с помощью [/OPT: REF](opt-optimizations.md).

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **входные данные** .

1. Измените свойство **Принудительная ссылка на символ** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ForceSymbolReferences%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
