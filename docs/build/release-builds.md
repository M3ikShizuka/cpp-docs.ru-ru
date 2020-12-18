---
description: 'Подробнее о следующем: Построения выпуска'
title: Сборки выпуска C++ — Visual Studio
ms.date: 12/10/2018
helpviewer_keywords:
- debugging [C++], release builds
- release builds
- debug builds, converting to release build
ms.assetid: fa9a78fa-f4b5-4722-baf4-aec655c4ff0f
ms.openlocfilehash: 7168fd50421835edc82d0599b22deb9214e28869
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97273791"
---
# <a name="release-builds"></a>Построения выпуска

В сборке выпуска используются оптимизации. При использовании оптимизации для создания сборки выпуска компилятор не будет создавать символьную отладочную информацию. Отсутствие символьной отладочной информации вместе с тем фактом, что для вызовов TRACE и ASSERT не создается код, означает, что размер исполняемого файла сокращается и, следовательно, выполняется быстрее.

## <a name="in-this-section"></a>Содержание раздела

[Распространенные проблемы, возникающие при создании сборок выпуска](common-problems-when-creating-a-release-build.md)<br/>
[Устранение проблем сборки выпуска](fixing-release-build-problems.md)<br/>
[Использование VERIFY вместо ASSERT](using-verify-instead-of-assert.md)<br/>
[Использование отладочной сборки для проверки перезаписи памяти](using-the-debug-build-to-check-for-memory-overwrite.md)<br/>
[Практическое руководство. Отладка сборки выпуска](how-to-debug-a-release-build.md)<br/>
[Проверка перезаписи памяти](checking-for-memory-overwrites.md)<br/>
[Оптимизация кода](optimizing-your-code.md)

## <a name="see-also"></a>См. также

[Справочные сведения о сборке C/C++](reference/c-cpp-building-reference.md)
