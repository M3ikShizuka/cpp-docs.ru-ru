---
description: Дополнительные сведения о:/ALLOWBIND (запрет привязки DLL)
title: /ALLOWBIND (запретить привязку DLL)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.PreventDLLBinding
- /allowbind
helpviewer_keywords:
- /ALLOWBIND linker option
- binding DLLs
- preventing DLL binding
- ALLOWBIND linker option
- -ALLOWBIND linker option
- DLLs [C++], preventing binding
ms.assetid: 30e37e24-12e4-407e-988a-39d357403598
ms.openlocfilehash: 727f1cae7d1b0a94a8f7faba90ee6994df8657e7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97187238"
---
# <a name="allowbind-prevent-dll-binding"></a>/ALLOWBIND (запретить привязку DLL)

```
/ALLOWBIND[:NO]
```

## <a name="remarks"></a>Комментарии

Параметр /ALLOWBIND:NO устанавливает в заголовке библиотеки DLL бит, который указывает программе Bind.exe на то, что привязка образа не допускается. Если DLL имеет цифровую подпись, привязывать ее не следует (при привязке цифровая подпись становится недействительной).

Существующую библиотеку DLL для функции/ALLOWBIND можно изменить с помощью параметра [/ALLOWBIND](allowbind.md) служебной программы EDITBIN.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Разверните узел **Свойства конфигурации**, **Компоновщик** и выберите пункт **Командная строка**.

1. Введите `/ALLOWBIND:NO` **Дополнительные параметры**.

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)<br/>
[Функция BindImage](/windows/win32/api/imagehlp/nf-imagehlp-bindimage)<br/>
[Функция Биндимажеекс](/windows/win32/api/imagehlp/nf-imagehlp-bindimageex)
