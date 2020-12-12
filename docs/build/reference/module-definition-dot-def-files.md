---
description: 'Дополнительные сведения о: Module-Definition (. DEF-файлы)'
title: Файлы определения модуля (DEF)
ms.date: 11/04/2016
helpviewer_keywords:
- def files
- module definition files
- .def files
ms.assetid: 08c0bc28-c5d2-47aa-9624-7fc68bcaa4d8
ms.openlocfilehash: d52141a2917b2c82616597b2d070a84b96d1a653
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97137817"
---
# <a name="module-definition-def-files"></a>Файлы определения модуля (DEF)

Файлы определения модуля (DEF) предоставляют компоновщику сведения о экспорте, атрибутах и другие сведения о программе, которую необходимо связать. DEF-файл наиболее удобен при создании библиотеки DLL. Так как существуют [компилятором MSVC параметры компоновщика](linker-options.md) , которые можно использовать вместо операторов определения модуля, DEF-файлы обычно не требуются. Можно также использовать [__declspec (dllexport)](../exporting-from-a-dll-using-declspec-dllexport.md) в качестве способа указания экспортированных функций.

DEF-файл можно вызвать на этапе компоновщика с помощью параметра компоновщика [/DEF (укажите Module-Definition файл)](def-specify-module-definition-file.md) .

Если вы создаете exe-файл, который не содержит экспорты, то использование файла. def приведет к увеличению и более медленной загрузке выходного файла.

Пример см. в разделе [Экспорт из библиотеки DLL с использованием DEF-файлов](../exporting-from-a-dll-using-def-files.md).

Дополнительные сведения см. в следующих разделах.

- [Правила для Module-Definitionных инструкций](rules-for-module-definition-statements.md)

- [ЭКСПОРТ](exports.md)

- [HEAPSIZE](heapsize.md)

- [Библиотечная](library.md)

- [ИМЯ](name-c-cpp.md)

- [СВЯЩЕН](sections-c-cpp.md)

- [STACKSIZE](stacksize.md)

- [ЛОВУШЕК](stub.md)

- [VERSION](version-c-cpp.md)

- [Зарезервированные слова](reserved-words.md)

## <a name="see-also"></a>См. также

[Справочные сведения о сборке C/C++](c-cpp-building-reference.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
