---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4559'
title: Предупреждение компилятора (уровень 4) C4559
ms.date: 08/27/2018
f1_keywords:
- C4559
helpviewer_keywords:
- C4559
ms.assetid: ed542f60-454d-45cb-85da-987ede61b1ab
ms.openlocfilehash: 64a8da1a7719d515cc9ddb7b5b6c3e54309ef6cb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97206634"
---
# <a name="compiler-warning-level-4-c4559"></a>Предупреждение компилятора (уровень 4) C4559

> "*функция*": переопределение; Функция прибылей __declspec (*Модификатор*)

## <a name="remarks"></a>Комментарии

Функция была переопределена или объявлена повторно, а второе определение или объявление добавило **`__declspec`** модификатор (*Модификатор*). Это предупреждение носит информационный характер. Чтобы устранить это предупреждение, удалите одно из определений.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4559:

```cpp
// C4559.cpp
// compile with: /W4 /LD
void f();
__declspec(noalias) void f();   // C4559
```
