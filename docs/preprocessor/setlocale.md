---
description: Дополнительные сведения о pragma директиве setlocale в Microsoft C/C++
title: pragma pragma
ms.date: 01/22/2021
f1_keywords:
- setlocale_CPP
- vc-pragma.setlocale
helpviewer_keywords:
- pragma, setlocale
- setlocale pragma
no-loc:
- pragma
ms.openlocfilehash: 936aa1c2eb26798438b48e61ec28007a12080f28
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713211"
---
# <a name="setlocale-no-locpragma"></a>`setlocale` pragma

Определяет *языковой стандарт*, страну, регион и язык, используемые при преобразовании символьных констант и строковых литералов.

## <a name="syntax"></a>Синтаксис

> **`#pragma setlocale( "`** [ *языковой стандарт — строка* ] **`" )`**

## <a name="remarks"></a>Примечания

Поскольку алгоритм преобразования многобайтовых символов в широкие символы может отличаться в зависимости от языкового стандарта или компиляция может выполняться в другом языковом стандарте, из которого будет выполняться исполняемый файл, это pragma позволяет указать целевой языковой стандарт во время компиляции. Он гарантирует, что строки расширенных символов хранятся в правильном формате.

*Локальная строка* по умолчанию — это пустая строка, указанная параметром `#pragma setlocale( "" )` .

**`"C"`** Языковой стандарт сопоставляет каждый символ в строке с его значением в виде **`wchar_t`** . Другие допустимые значения для `setlocale` — это записи, найденные в списке [языковых строк](../c-runtime-library/language-strings.md) . Например, можно указать:

```cpp
#pragma setlocale("dutch")
```

Возможность указания языковой строки зависит от поддержки кодовой страницы и идентификатора языка на компьютере.

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
