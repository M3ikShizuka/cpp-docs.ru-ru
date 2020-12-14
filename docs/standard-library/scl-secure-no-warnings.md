---
description: 'Дополнительные сведения: _SCL_SECURE_NO_WARNINGS'
title: _SCL_SECURE_NO_WARNINGS
ms.date: 11/04/2016
f1_keywords:
- _SCL_SECURE_NO_DEPRECATE
- _SCL_SECURE_NO_WARNINGS
helpviewer_keywords:
- _SCL_SECURE_NO_DEPRECATE
- _SCL_SECURE_NO_WARNINGS
ms.assetid: ef0ddea9-7c62-4b53-8b64-5f4fd369776f
ms.openlocfilehash: 383aeed0bdedc4830076248100c8cf0a1acf34b1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97187927"
---
# <a name="_scl_secure_no_warnings"></a>_SCL_SECURE_NO_WARNINGS

Вызов любого из потенциально небезопасных методов в стандартной библиотеке C++ приводит к [предупреждению компилятора (уровень 3) C4996](../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md). Чтобы отключить это предупреждение, определите в своем коде макрос _SCL_SECURE_NO_WARNINGS:

```cpp
#define _SCL_SECURE_NO_WARNINGS
```

При использовании предварительно скомпилированных заголовков поместите эту директиву в файл предкомпилированного заголовка перед включением любой библиотеки среды выполнения C или заголовков стандартной библиотеки. Если поместить его в отдельный файл исходного кода перед включением файла предкомпилированного заголовка, он игнорируется компилятором.

## <a name="remarks"></a>Комментарии

Другие способы отключения предупреждения C4996 перечислены ниже:

- Использование параметра компилятора [/D (определения препроцессора)](../build/reference/d-preprocessor-definitions.md):

   > CL/D_SCL_SECURE_NO_WARNINGS [другие параметры компилятора] MyFile. cpp

- Использование параметра компилятора [/w](../build/reference/compiler-option-warning-level.md):

   > CL/wd4996 [другие параметры компилятора] MyFile. cpp

- Использование директивы [предупреждение #pragma](../preprocessor/warning.md):

   ```cpp
   #pragma warning(disable:4996)
   ```

Кроме того, можно вручную изменить уровень предупреждения C4996 с помощью параметра компилятора **/w \<l> \<n>** . Например, чтобы задать для предупреждения C4996 уровень 4:

> CL/w44996 [другие параметры компилятора] MyFile. cpp

Дополнительные сведения см. в разделах [/w, /W0, /W1, /W2, /W3, /W4, /w1, /w2, /w3, /w4, /Wall, /wd, /we, /wo, /Wv, /WX (уровень предупреждений)](../build/reference/compiler-option-warning-level.md).

## <a name="see-also"></a>См. также раздел

[Надежные библиотеки: Стандартная библиотека C++](../standard-library/safe-libraries-cpp-standard-library.md)
