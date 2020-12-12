---
description: 'Дополнительные сведения о: параметры компилятора'
title: Параметры компилятора КОМПИЛЯТОРОМ MSVC
ms.date: 05/06/2019
helpviewer_keywords:
- cl.exe compiler
- x86 MSVC compiler
- ARM MSVC compiler
- compiler options, C++
- x64 MSVC compiler
ms.assetid: ed3376c8-bef4-4c9a-80e9-3b5da232644c
ms.openlocfilehash: a6b124fa5fce68844d53c1324da48c17ef5a9ccf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97197027"
---
# <a name="compiler-options"></a>Параметры компилятора

cl.exe — это средство, управляющее компиляторами и компоновщиком Microsoft C++ (КОМПИЛЯТОРОМ MSVC) C и C++. cl.exe можно запускать только в операционных системах, поддерживающих Microsoft Visual Studio для Windows.

> [!NOTE]
> Это средство можно запустить только из командной строки разработчика Visual Studio. В системной командной строке или проводнике это невозможно. Дополнительные сведения см. в статье [Использование набора инструментов MSVC из командной строки](../building-on-the-command-line.md).

Компиляторы создают объектные файлы формата COFF (obj). Компоновщик создает исполняемые (exe) файлы или библиотеки динамической компоновки (DLL).

Обратите внимание, что все параметры компилятора чувствительны к регистру. Для указания параметра компилятора можно использовать либо косую черту ( `/` ), либо тире ( `-` ).

Чтобы выполнить компиляцию без компоновки, используйте параметр [/c](c-compile-without-linking.md) .

## <a name="find-a-compiler-option"></a>Найти параметр компилятора

Чтобы найти конкретный параметр компилятора, см. один из следующих списков.

- [Параметры компилятора в алфавитном порядке](compiler-options-listed-alphabetically.md)

- [Параметры компилятора, перечисленные по категориям](compiler-options-listed-by-category.md)

## <a name="specify-compiler-options"></a>Укажите параметры компилятора

В разделе, посвященном каждому параметру компилятора, описывается, как его можно задать в среде разработки. Сведения об указании параметров вне среды разработки см. в следующих статьях:

- [Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)

- [Командные файлы CL](cl-command-files.md)

- [Переменные среды CL](cl-environment-variables.md)

## <a name="related-build-tools"></a>Связанные средства сборки

[Параметры компоновщика компилятором MSVC](linker-options.md) также влияют на процесс сборки программы.

## <a name="see-also"></a>См. также

[Справочные сведения о сборке C/C++](c-cpp-building-reference.md)<br/>
[CL вызывает компоновщик](cl-invokes-the-linker.md)
