---
description: 'Дополнительные сведения о: Ошибка компилятора C3223'
title: Ошибка компилятора C3223
ms.date: 11/04/2016
f1_keywords:
- C3223
helpviewer_keywords:
- C3223
ms.assetid: 1f4380b4-0413-40db-a868-62f97babaf78
ms.openlocfilehash: d768bba53634e3614ba4dc583cb57d2d16e744fa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97267694"
---
# <a name="compiler-error-c3223"></a>Ошибка компилятора C3223

"свойство": нельзя применить typeid к свойству

Нельзя применить [typeid](../../extensions/typeid-cpp-component-extensions.md) к свойству.

## <a name="example"></a>Пример

В следующем примере возникает ошибка C3223:

```cpp
// C3223.cpp
// compile with: /clr
ref class R {
public:
   property int myprop;
};

int main() {
   System::Type^ type2 = R::myprop::typeid;   // C3223
}
```
