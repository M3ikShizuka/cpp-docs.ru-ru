---
description: Дополнительные сведения об устаревшей pragma директиве в Microsoft C/C++
title: не рекомендуется pragma
ms.date: 01/22/2021
f1_keywords:
- vc-pragma.deprecated
helpviewer_keywords:
- deprecated pragma
- pragma, deprecated
no-loc:
- pragma
ms.openlocfilehash: 47e049f415b243a4c9959c7adc789f32f91de7ba
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98712912"
---
# <a name="deprecated-no-locpragma"></a>`deprecated` pragma

**`deprecated`** pragma Позволяет указать, что функция, тип или любой другой идентификатор может больше не поддерживаться в будущем выпуске или больше не должна использоваться.

> [!NOTE]
> Сведения об атрибуте C++ 14 `[[deprecated]]` и рекомендации по использованию этого атрибута вместо `__declspec(deprecated)` модификатора Майкрософт или см **`deprecated`** pragma . в разделе [атрибуты в c++](../cpp/attributes.md).

## <a name="syntax"></a>Синтаксис

> **`#pragma deprecated(`***идентификатор1* [ **`,`** *идентификатор2* ...]**`)`**

## <a name="remarks"></a>Примечания

Когда компилятор встречает идентификатор, заданный параметром **`deprecated`** pragma , он выдает предупреждение компилятора [C4995](../error-messages/compiler-warnings/compiler-warning-level-3-c4995.md).

Имена макросов можно объявить нерекомендуемыми. Поместите имя макроса в кавычки; в противном случае произойдет расширение макроса.

Поскольку объект **`deprecated`** pragma работает на всех совпадающих идентификаторах и не принимает подписи в учетной записи, он не является лучшим вариантом для устаревших версий перегруженных функций. Все совпадающие имена функций, которые были добавлены в область действия, инициируют предупреждение.

Рекомендуется использовать атрибут C++ 14 `[[deprecated]]` , если это возможно, вместо **`deprecated`** pragma . Модификатор объявления, характерный для Microsoft, [`__declspec(deprecated)`](../cpp/deprecated-cpp.md) также является лучшим выбором во многих случаях, чем **`deprecated`** pragma . `[[deprecated]]`Атрибут и `__declspec(deprecated)` Модификатор позволяют указать нерекомендуемое состояние для определенных форм перегруженных функций. Предупреждение диагностики отображается только в ссылках на конкретную перегруженную функцию, к которой применяется атрибут или модификатор.

## <a name="example"></a>Пример

```cpp
// pragma_directive_deprecated.cpp
// compile with: /W3
#include <stdio.h>
void func1(void) {
}

void func2(void) {
}

int main() {
   func1();
   func2();
   #pragma deprecated(func1, func2)
   func1();   // C4995
   func2();   // C4995
}
```

В следующем примере показано, как объявить класс устаревшим.

```cpp
// pragma_directive_deprecated2.cpp
// compile with: /W3
#pragma deprecated(X)
class X {  // C4995
public:
   void f(){}
};

int main() {
   X x;   // C4995
}
```

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
