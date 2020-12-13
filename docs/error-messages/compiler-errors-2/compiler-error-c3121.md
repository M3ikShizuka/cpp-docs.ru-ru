---
description: 'Дополнительные сведения о: Ошибка компилятора C3121'
title: Ошибка компилятора C3121
ms.date: 11/04/2016
f1_keywords:
- C3121
helpviewer_keywords:
- C3121
ms.assetid: 1d3c7be4-d42d-4def-8d53-182c0c5cc237
ms.openlocfilehash: 62f12d17d8696e500cc21084645533825e7f25f9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97151064"
---
# <a name="compiler-error-c3121"></a>Ошибка компилятора C3121

невозможно изменить GUID для класса "class_name"

Предпринята попытка изменить идентификатор класса на [__declspec (UUID)](../../cpp/uuid-cpp.md).

Например, следующий код создает C3121:

```cpp
// C3121.cpp
[emitidl];
[module(name="MyLibrary")];

[coclass, uuid="00000000-0000-0000-0000-111111111111"]
class __declspec(uuid("00000000-0000-0000-0000-111111111112")) A   // C3121
{
};
int main()
{
}
```
