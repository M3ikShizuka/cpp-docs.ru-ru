---
description: 'Дополнительные сведения: Command-Line Error D8045'
title: Ошибка командной строки D8045
ms.date: 11/04/2016
f1_keywords:
- D8045
helpviewer_keywords:
- D8045
ms.assetid: 01c8808c-bac1-4b4d-8a90-b595f95e9318
ms.openlocfilehash: 0445454a1e44e85b43fa0302867d9109e9ee3e38
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97115603"
---
# <a name="command-line-error-d8045"></a>Ошибка командной строки D8045

невозможно скомпилировать файл C "файл" с параметром/CLR

Только файлы исходного кода C++ могут быть переданы в компиляцию, использующую **/CLR**.  Используйте **/TP** , чтобы скомпилировать c-файл как CPP-файл; Дополнительные сведения см. в разделе [/TC,/TP,/TC,/TP (указание типа исходного файла)](../../build/reference/tc-tp-tc-tp-specify-source-file-type.md) .

Дополнительные сведения см. в разделе [/CLR (компиляция среды CLR)](../../build/reference/clr-common-language-runtime-compilation.md).

D8045 также может возникнуть при компиляции приложения ATL с помощью Visual C++. Дополнительные сведения см. в разделе [инструкции. Миграция в/CLR](../../dotnet/how-to-migrate-to-clr.md) .
