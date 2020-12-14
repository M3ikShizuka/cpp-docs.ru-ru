---
description: 'Дополнительные сведения о: Ошибка компилятора C3539'
title: Ошибка компилятора C3539
ms.date: 11/04/2016
f1_keywords:
- C3539
helpviewer_keywords:
- C3539
ms.assetid: 34a33a0f-d1b6-498f-b312-ffad2d4799b3
ms.openlocfilehash: a944a2e6af03e030434cf41e2b6009be82ad9239
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97315248"
---
# <a name="compiler-error-c3539"></a>Ошибка компилятора C3539

"тип": аргумент шаблона не может быть типом, содержащим "Auto"

Указанный тип аргумента шаблона не может содержать использование **`auto`** ключевого слова.

### <a name="to-correct-this-error"></a>Исправление ошибки

1. Не указывайте аргумент шаблона с **`auto`** ключевым словом.

## <a name="example"></a>Пример

В следующем примере выдается C3539.

```cpp
// C3539.cpp
// Compile with /Zc:auto
template<class T> class C{};
int main()
{
   C<auto> c;   // C3539
   return 0;
}
```

## <a name="see-also"></a>См. также

[Ключевое слово auto](../../cpp/auto-cpp.md)
