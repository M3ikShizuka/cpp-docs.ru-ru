---
description: 'Дополнительные сведения о: Ошибка компилятора C3646'
title: Ошибка компилятора C3646
ms.date: 06/14/2018
f1_keywords:
- C3646
helpviewer_keywords:
- C3646
ms.assetid: 4391ead2-9637-4ca3-aeda-5a991b18d66d
ms.openlocfilehash: 0c6f731a09612e6c128756de8d0690c922047e49
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97203787"
---
# <a name="compiler-error-c3646"></a>Ошибка компилятора C3646

> "спецификатор": Неизвестный спецификатор переопределения

## <a name="remarks"></a>Комментарии

Компилятор обнаружил маркер в том месте, где ожидалось найти спецификатор переопределения, но маркер не был распознан компилятором.

Например, если нераспознанный *спецификатор* **_NOEXCEPT**, замените его ключевым словом **`noexcept`** .

Дополнительные сведения см. в разделе [Описатели переопределения](../../extensions/override-specifiers-cpp-component-extensions.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3646 и демонстрирует способ исправления:

```cpp
// C3646.cpp
// compile with: /clr /c
ref class C {
   void f() unknown;   // C3646
   // try the following line instead
   // virtual void f() abstract;
};
```
