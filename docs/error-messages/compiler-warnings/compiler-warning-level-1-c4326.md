---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4326'
title: Предупреждение компилятора (уровень 1) C4326
ms.date: 08/27/2018
f1_keywords:
- C4326
helpviewer_keywords:
- C4326
ms.assetid: d44d2c4e-9456-42d3-b35b-4ba4b2d42ec7
ms.openlocfilehash: d7c82d7a0157b53e60281bbe7c45a38cc765a73d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340050"
---
# <a name="compiler-warning-level-1-c4326"></a>Предупреждение компилятора (уровень 1) C4326

> возвращаемый тип "*функция*" должен быть "*тип1*", а не "*тип2*"

## <a name="remarks"></a>Комментарии

Функция вернула тип, отличный от *Type1*. Например, при использовании [/Za](../../build/reference/za-ze-disable-language-extensions.md) **Main** не возвращает **`int`** .

## <a name="example"></a>Пример

В следующем примере создается C4326 и демонстрируется его устранение.

```cpp
// C4326.cpp
// compile with: /Za /W1
char main()
{
    // C4326, instead use int main()
}
```
