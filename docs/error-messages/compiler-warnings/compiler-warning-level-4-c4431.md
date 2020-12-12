---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4431'
title: Предупреждение компилятора (уровень 4) C4431
ms.date: 11/04/2016
f1_keywords:
- C4431
helpviewer_keywords:
- C4431
ms.assetid: 58434ab6-dd8d-427b-953a-602fb7453ae6
ms.openlocfilehash: 47e83f5e49ec8a4e54f4cda62267d01bd42f1ce7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97251496"
---
# <a name="compiler-warning-level-4-c4431"></a>Предупреждение компилятора (уровень 4) C4431

отсутствует спецификатор типа — предполагается int. Примечание. C++ не поддерживает тип int по умолчанию

Эта ошибка может быть вызвана работой по согласованности компилятора, выполненной для Visual Studio 2005: Visual C++ больше не создает нетипизированные идентификаторы как int по умолчанию. Тип идентификатора должен быть указан явным образом.

Это предупреждение отключено по умолчанию. Подробнее: [Выключенные по умолчанию предупреждения компилятора](../../preprocessor/compiler-warnings-that-are-off-by-default.md) .

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4431.

```c
// C4431.c
// compile with: /c /W4
#pragma warning(default:4431)
i;   // C4431
int i;   // OK
```
