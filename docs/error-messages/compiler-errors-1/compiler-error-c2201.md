---
description: 'Дополнительные сведения о: Ошибка компилятора C2201'
title: Ошибка компилятора C2201
ms.date: 11/04/2016
f1_keywords:
- C2201
helpviewer_keywords:
- C2201
ms.assetid: ed927659-6e9c-447d-9963-19969ae1e957
ms.openlocfilehash: 334a459a6fbfa930c99e3c203b1fb214cb36706a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97319005"
---
# <a name="compiler-error-c2201"></a>Ошибка компилятора C2201

"идентификатор": для экспорта или импорта требуется внешняя компоновка

Экспортированный идентификатор — **`static`** .

При компиляции следующего примера возникнет ошибка C2286:

```cpp
// C2201.cpp
// compile with: /c
__declspec(dllexport) static void func() {}   // C2201 func() is static
__declspec(dllexport) void func2() {}   // OK
```

## <a name="see-also"></a>См. также раздел

[Типы компоновки](../../cpp/program-and-linkage-cpp.md)
