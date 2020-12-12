---
description: Дополнительные сведения о:/GF (исключение повторяющихся строк)
title: /GF (Исключение повторяющихся строк)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCCLCompilerTool.StringPooling
- VC.Project.VCCLWCECompilerTool.StringPooling
- /gf
helpviewer_keywords:
- duplicate strings
- Eliminate Duplicate Strings compiler option [C++]
- pooling strings compiler option [C++]
- -GF compiler option [C++]
- /GF compiler option [C++]
- GF compiler option [C++]
- strings [C++], pooling
ms.assetid: bb7b5d1c-8e1f-453b-9298-8fcebf37d16c
ms.openlocfilehash: 65c8cca610b9e01cf49939c2074a698b00c6e338
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97191944"
---
# <a name="gf-eliminate-duplicate-strings"></a>/GF (Исключение повторяющихся строк)

Позволяет компилятору создавать единую копию одинаковых строк в образе программы и в памяти во время выполнения. Это оптимизация, называемая *объединением строк* , которая может создавать небольшие программы.

## <a name="syntax"></a>Синтаксис

```
/GF
```

## <a name="remarks"></a>Remarks

При использовании параметра **/GF** операционная система не меняет местами строку памяти и может считывать строки из файла изображения.

**/GF** объединяет строки как доступ только для чтения. При попытке изменить строки в параметре **/GF** возникает ошибка приложения.

Объединение строк позволяет использовать несколько указателей на один буфер в качестве нескольких указателей на несколько буферов. В следующем коде `s` и `t` инициализируются с одной и той же строкой. Объединение строк приводит к тому, что они указывают на одну и ту же память:

```
char *s = "This is a character buffer";
char *t = "This is a character buffer";
```

> [!NOTE]
> Параметр [/Zi](z7-zi-zi-debug-information-format.md) , используемый для функции "изменить и продолжить", автоматически задает параметр **/GF** .

> [!NOTE]
> Параметр компилятора **/GF** создает адресный раздел для каждой уникальной строки. По умолчанию объектный файл может содержать до 65 536 адресных секций. Если программа содержит более 65 536 строк, используйте параметр компилятора [/bigobj](bigobj-increase-number-of-sections-in-dot-obj-file.md) , чтобы создать дополнительные разделы.

**/GF** действует, когда используется [/O1](o1-o2-minimize-size-maximize-speed.md) или [/O2](o1-o2-minimize-size-maximize-speed.md) .

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Перейдите на страницу свойств **Создание кода** .

1. Измените свойство **включить объединение строк** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.StringPooling%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
