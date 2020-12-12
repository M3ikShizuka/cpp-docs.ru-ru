---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4727'
title: Предупреждение компилятора (уровень 1) C4727
ms.date: 08/19/2019
f1_keywords:
- C4727
helpviewer_keywords:
- C4727
ms.assetid: 991b0087-3a50-40f5-9cdb-cdc367cd472c
ms.openlocfilehash: 7639e6462cd5da0f5bd452bd0b80eddc80d5fe76
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97194115"
---
# <a name="compiler-warning-level-1-c4727"></a>Предупреждение компилятора (уровень 1) C4727

В obj_file_1 и obj_file_2 обнаружен PCH с именем pch_file с той же меткой времени.  Используется первый PCH.

> [!NOTE]
> В Visual Studio 2017 и более ранних версиях предкомпилированный заголовок по умолчанию называется *stdafx. h* , а в visual Studio 2019 и более поздних версий он называется *PCH. h* по умолчанию.

C4727 возникает при компиляции нескольких компиляндов с параметром **/Yc** и в том месте, где компилятору удалось пометить все OBJ-файлы с одинаковой меткой времени PCH.

Для устранения ошибки скомпилируйте один исходный файл с параметром **/Yc/c** (создает PCH), а остальные компилируются отдельно с **/Yu/c** (использует PCH), а затем свяжите их вместе.

Итак, если вы выполнили следующие действия и создаете C4727:

::: moniker range="<=msvc-150"

**CL/CLR/GL a. cpp b. cpp c. cpp/Икстдафкс.х**

Вместо этого можно сделать следующее:

**CL/CLR/GL a. cpp/Икстдафкс.х/c**

**CL/CLR/GL b. cpp c. cpp/Юстдафкс.х/Link a. obj**

::: moniker-end

::: moniker range=">=msvc-160"

**CL/CLR/GL a. cpp b. cpp c. cpp/ИКПЧ.х**

Вместо этого можно сделать следующее:

**CL/CLR/GL a. cpp/ИКПЧ.х/c**

**CL/CLR/GL b. cpp c. cpp/ЮПЧ.х/Link a. obj**

::: moniker-end

Дополнительные сведения см. в разделе

- [/Yc (создание файла предкомпилированного заголовка)](../../build/reference/yc-create-precompiled-header-file.md)

- [/Yu (использование файла предкомпилированного заголовка)](../../build/reference/yu-use-precompiled-header-file.md)
