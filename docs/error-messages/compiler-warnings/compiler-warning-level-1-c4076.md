---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4076'
title: Предупреждение компилятора (уровень 1) C4076
ms.date: 11/04/2016
f1_keywords:
- C4076
helpviewer_keywords:
- C4076
ms.assetid: 04581066-313a-4a11-bb60-721e6d038d75
ms.openlocfilehash: 0bae49d3af23e499851fbf70fb24fdeb817ee03c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97198262"
---
# <a name="compiler-warning-level-1-c4076"></a>Предупреждение компилятора (уровень 1) C4076

> "*Модификатор типа*": не может использоваться с типом "*TypeName*"

## <a name="remarks"></a>Комментарии

Модификатор типа ( **`signed`** или **`unsigned`** ) не может использоваться с типом, не являющимся целым числом. *Модификатор типа* игнорируется.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4076; чтобы устранить эту проблему, удалите **`unsigned`** Модификатор типа:

```cpp
// C4076.cpp
// compile with: /W1 /LD
unsigned double x;   // C4076
```
