---
description: 'Дополнительные сведения о: житинтринсик'
title: jitintrinsic
ms.date: 11/04/2016
f1_keywords:
- jitintrinsic
- jitintrinsic_cpp
helpviewer_keywords:
- __declspec keyword [C++], jitintrinsic
- jitintrinsic __declspec modifier
ms.assetid: 23dbe416-7ef6-442b-b16d-9a81aab04fa6
ms.openlocfilehash: 29f4db3e946d2ccf0ec96bb0248e751bb9297db5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97292004"
---
# <a name="jitintrinsic"></a>jitintrinsic

Помечает функцию как значимую для 64-разрядной среды CLR. Этот модификатор используется с определенными функциями в библиотеках Microsoft.

## <a name="syntax"></a>Синтаксис

```
__declspec(jitintrinsic)
```

## <a name="remarks"></a>Remarks

**`jitintrinsic`** Добавляет MODOPT ( <xref:System.Runtime.CompilerServices.IsJitIntrinsic> ) в сигнатуру функции.

Пользователям не рекомендуется использовать этот **`__declspec`** модификатор, так как могут возникать непредвиденные результаты.

## <a name="see-also"></a>См. также раздел

[__declspec](../cpp/declspec.md)<br/>
[Ключевые слова](../cpp/keywords-cpp.md)
