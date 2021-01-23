---
description: Дополнительные сведения о pragma директиве соответствия в Microsoft C/C++
title: обеспечить pragma
ms.date: 01/22/2021
f1_keywords:
- conform_CPP
- vc-pragma.conform
helpviewer_keywords:
- conform pragma
- forScope conform pragma
- pragma, conform
no-loc:
- pragma
ms.openlocfilehash: baaeb41e2364daac8de91ca15251226bf3dd1e2a
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713705"
---
# <a name="conform-no-locpragma"></a>`conform` pragma

**Блок, относящийся только к языку C++**

Задает поведение во время выполнения [`/Zc:forScope`](../build/reference/zc-forscope-force-conformance-in-for-loop-scope.md) параметра компилятора.

## <a name="syntax"></a>Синтаксис

> **`#pragma conform(`***имя* [ **`, show`** ] [ **`,`** { **`on`**  |  **`off`** }] [[ **`,`** { **`push`**  |  **`pop`** }] [ **`,`** *идентификатор* [ **`,`** { **`on`**  |  **`off`** }]]]**`)`**

### <a name="parameters"></a>Параметры

*безымян*\
Определяет имя параметра компилятора, которое требуется изменить. Единственное допустимое *имя* : `forScope` .

**`show`**\
Используемых Приводит к тому, что текущее значение параметра *Name* (true или false) будет отображаться с помощью предупреждающего сообщения во время компиляции. Например, `#pragma conform(forScope, show)`.

**`on`**, **`off`**\
Используемых Параметр *Name* **`on`** включает параметр компилятора [/Zc: forScope](../build/reference/zc-forscope-force-conformance-in-for-loop-scope.md) . Значение по умолчанию — **`off`** .

**`push`**\
Используемых Помещает текущее значение *имени* во внутренний стек компилятора. При указании *идентификатора* можно указать **`on`** **`off`** значение или для *имени* , которое будет помещено в стек. Например, `#pragma conform(forScope, push, myname, on)`.

**`pop`**\
Используемых Задает значение *Name* в начале внутреннего стека компилятора, а затем извлекает стек. Если идентификатор указан с помощью **`pop`** , стек будет извлечен обратно до тех пор, пока не будет найдена запись с *идентификатором*, которая также может быть извлечена; текущее значение *имени* в следующей записи в стеке становится новым значением для *Name*. Если указать **`pop`** с *идентификатором* , который не находится в записи в стеке, то **`pop`** игнорируется.

*identifier*\
Используемых Может включаться в **`push`** **`pop`** команду или. Если используется *идентификатор* , **`on`** **`off`** можно также использовать описатель или.

## <a name="example"></a>Пример

```cpp
// pragma_directive_conform.cpp
// compile with: /W1
// C4811 expected
#pragma conform(forScope, show)
#pragma conform(forScope, push, x, on)
#pragma conform(forScope, push, x1, off)
#pragma conform(forScope, push, x2, off)
#pragma conform(forScope, push, x3, off)
#pragma conform(forScope, show)
#pragma conform(forScope, pop, x1)
#pragma conform(forScope, show)

int main() {}
```

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
