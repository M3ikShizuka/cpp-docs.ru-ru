---
description: 'Дополнительные сведения о: Ошибка компилятора C2692'
title: Ошибка компилятора C2692
ms.date: 11/04/2016
f1_keywords:
- C2692
helpviewer_keywords:
- C2692
ms.assetid: 02ade3b4-b757-448b-b065-d7d71bc3f441
ms.openlocfilehash: 5a9666bf437d65c54d0cb8c460054b2b3ebd0b55
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97326688"
---
# <a name="compiler-error-c2692"></a>Ошибка компилятора C2692

"function_name": в компиляторе C должны быть полностью прототипные функции с параметром "/CLR"

При компиляции для управляемого кода .NET компилятору C требуются объявления функций ANSI. Кроме того, если функция не принимает параметров, она должна явно объявляться **`void`** в качестве типа параметра.
