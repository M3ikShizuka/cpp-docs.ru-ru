---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4160'
title: Предупреждение компилятора (уровень 1) C4160
ms.date: 08/27/2018
f1_keywords:
- C4160
helpviewer_keywords:
- C4160
ms.assetid: a9610cb7-cac4-4a74-8b4e-049030ebb92b
ms.openlocfilehash: afb9a0a30376a0e0b1c59b89e98a131ab5889017
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97267200"
---
# <a name="compiler-warning-level-1-c4160"></a>Предупреждение компилятора (уровень 1) C4160

> #<a name="pragma-pop--did-not-find-previously-pushed-identifier-identifier"></a>pragma (POP,...): не найден ранее отправленный идентификатор "*идентификатор*"

## <a name="remarks"></a>Комментарии

Оператор pragma в исходном коде пытается извлечь из стека идентификатор, который не был занесен в стек. Чтобы устранить это предупреждение, необходимо убедиться в том, что идентификатор, извлекаемый из стека, был туда соответствующим образом занесен.

## <a name="example"></a>Пример

В следующем примере создается C4160 и демонстрируется его устранение:

```cpp
// C4160.cpp
// compile with: /W1
#pragma pack(push)

#pragma pack(pop, id)   // C4160
// use identifier when pushing to resolve the warning
// #pragma pack(push, id)

int main() {
}
```
