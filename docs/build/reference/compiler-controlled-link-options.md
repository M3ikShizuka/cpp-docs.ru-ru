---
description: Дополнительные сведения о параметрах ссылки Compiler-Controlled.
title: Compiler-Controlled LINK Options
ms.date: 11/04/2016
helpviewer_keywords:
- LINK tool [C++], compiler-controlled options
- linker [C++], CL compiler control
- linking [C++], affected by CL features
- cl.exe compiler [C++], features that affect linking
- cl.exe compiler [C++], controlling linker
ms.assetid: e4c03896-c99c-4599-8502-e0f4bebe69d0
ms.openlocfilehash: 86f03f53fe19f6788528dca421fb6030289fca99
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97178983"
---
# <a name="compiler-controlled-link-options"></a>Compiler-Controlled LINK Options

Компилятор CL автоматически вызывает LINK, если не указан параметр/c. CL предоставляет некоторый контроль над компоновщиком с помощью параметров командной строки и аргументов. В следующей таблице перечислены функции, которые влияют на компоновку в CL.

|Спецификация CL|Действие CL, которое влияет на связь|
|----------------------|---------------------------------|
|Любое расширение имени файла, отличное от. c,. CXX,. cpp или. def|Передает имя файла в качестве входных данных для ссылки|
|*имя файла*. def|Передает/DEF:*filename*. def|
|/F *число*|Передача значения/STACK:*Number*|
|*Имя файла* /FD|Передает/PDB:*filename*|
|*Имя файла* /Fe|Передает/OUT:*filename*|
|*Имя файла* /FM|Передает/MAP:*filename*|
|/Gy|Создает упакованные функции (COMDAT); включает компоновку на уровне функций|
|/LD|Передача/DLL|
|/LDd|Передача/DLL|
|/link|Передает оставшуюся часть командной строки для СВЯЗЫВАНИЯ|
|/MD или/MT|Помещает имя библиотеки по умолчанию в OBJ-файл|
|/MDd или/MTd|Помещает имя библиотеки по умолчанию в OBJ-файл. Определяет символ **_DEBUG**|
|/nologo|Передает/NOLOGO|
|/Zd|Передает/DEBUG|
|/Zi или/Z7|Передает/DEBUG|
|/Zl|Исключает имя библиотеки по умолчанию из OBJ-файла|

Дополнительные сведения см. в разделе [параметры компилятора компилятором MSVC](compiler-options.md).

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
