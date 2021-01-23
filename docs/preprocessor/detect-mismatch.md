---
description: Дополнительные сведения об pragma директиве detect_mismatch в Microsoft C/C++
title: detect_mismatch pragma
ms.date: 01/22/2021
f1_keywords:
- vc-pragma.detect_mismatch
- detect_mismatch_CPP
helpviewer_keywords:
- pragma, detect_mismatch
- detect_mismatch pragma
no-loc:
- pragma
ms.openlocfilehash: 33bc899eaaed73329e24e7f210fa91adc8addaa9
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713679"
---
# <a name="detect_mismatch-no-locpragma"></a>`detect_mismatch` pragma

Помещает запись в объект. Компоновщик проверяет эти записи на предмет наличия потенциальных несоответствий.

## <a name="syntax"></a>Синтаксис

> **`#pragma detect_mismatch(`** "*имя*" **`,`** "*значение*" **`)`**

## <a name="remarks"></a>Примечания

При связывании проекта компоновщик создает ошибку [LNK2038](../error-messages/tool-errors/linker-tools-error-lnk2038.md) , если проект содержит два объекта с одинаковым *именем* , но у каждого из них другое *значение*. Используйте этот pragma способ, чтобы предотвратить связывание несоответствующих файлов объектов.

И *имя* , и *значение* являются строковыми литералами и подчиняются правилам для строковых литералов в отношении escape-символов и сцепления. Они чувствительны к регистру и не могут содержать запятую, знак равенства, кавычки или символ **null** .

## <a name="example"></a>Пример

В этом примере создаются два файла, имеющие разные номера версий для одной метки версии.

```cpp
// pragma_directive_detect_mismatch_a.cpp
#pragma detect_mismatch("myLib_version", "9")
int main ()
{
   return 0;
}

// pragma_directive_detect_mismatch_b.cpp
#pragma detect_mismatch("myLib_version", "1")
```

При компиляции обоих файлов с помощью командной строки `cl pragma_directive_detect_mismatch_a.cpp pragma_directive_detect_mismatch_b.cpp` вы получите ошибку LNK2038.

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
