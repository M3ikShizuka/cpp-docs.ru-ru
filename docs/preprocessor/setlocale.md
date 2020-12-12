---
description: 'Дополнительные сведения о команде: setlocale pragma'
title: Прагма setlocale
ms.date: 08/29/2019
f1_keywords:
- setlocale_CPP
- vc-pragma.setlocale
helpviewer_keywords:
- pragmas, setlocale
- setlocale pragma
ms.assetid: e60b43d9-fbdf-4c4e-ac85-805523a13b86
ms.openlocfilehash: 375a2075381b39037a6a723f7d28ef73749ec08f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97167309"
---
# <a name="setlocale-pragma"></a>Прагма setlocale

Определяет *языковой стандарт*, страну, регион и язык, используемые при преобразовании символьных констант и строковых литералов.

## <a name="syntax"></a>Синтаксис

> **#pragma setlocale ("** [ *locale-String* ] **")**

## <a name="remarks"></a>Комментарии

Поскольку алгоритм преобразования многобайтовых символов в широкие символы может отличаться в зависимости от языкового стандарта или компиляция может выполняться в другом языковом стандарте, из которого будет выполняться исполняемый файл, эта директива pragma предоставляет способ указания целевого языкового стандарта во время компиляции. Он гарантирует, что строки расширенных символов хранятся в правильном формате.

*Локальная строка* по умолчанию — "".

Языковой стандарт "C" сопоставляет каждый символ в строке с его значением в виде **`wchar_t`** . Другие допустимые значения для `setlocale` — это записи, найденные в списке [языковых строк](../c-runtime-library/language-strings.md) . Например, можно указать:

```cpp
#pragma setlocale("dutch")
```

Возможность указания языковой строки зависит от поддержки кодовой страницы и идентификатора языка на компьютере.

## <a name="see-also"></a>См. также раздел

[Директивы pragma и ключевое слово __pragma](../preprocessor/pragma-directives-and-the-pragma-keyword.md)
