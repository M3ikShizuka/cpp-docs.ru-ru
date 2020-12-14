---
description: 'Дополнительные сведения о: from_chars_result struct'
title: Структура from_chars_result
ms.date: 7/23/2020
f1_keywords:
- std::from_chars_result
helpviewer_keywords:
- from_chars_result class
- from_chars_result structure
ms.openlocfilehash: 894a687a4395e22538b384675af5b4ce57731f78
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97232282"
---
# <a name="from_chars_result-struct"></a>Структура from_chars_result

## <a name="syntax"></a>Синтаксис

```cpp
struct from_chars_result {
    const char* ptr;
    errc ec;
};
```

|Член|Описание|
|--|--|
|`ptr`| Если `ec` значение равно `errc{}` , преобразование прошло успешно и `ptr` указывает на первый символ, который не является частью распознанного числа. |
|`ec` | Код ошибки преобразования. Конкретные коды ошибок см. в разделе [`errc`](system-error-enums.md#errc) .|

### <a name="remarks"></a>Комментарии

Пример. синтаксический анализ `"1729cats"` в виде десятичного целого числа будет выполнен, и `ptr` будет указывать на то, `'c'` что является первой нецифровой цифрой `"1729"` .

Если ни один из символов не соответствует шаблону числа, `from_chars_result.ptr` указывает на `first` , и `from_chars_result.ec` имеет значение `errc::invalid_argument` .

Если шаблон числа соответствует только некоторым символам, `from_chars_result.ptr` указывает на первый символ, не совпадающий с шаблоном, или значение `last` параметра, если все символы совпадают.

Если проанализированное значение не соответствует диапазону выполняемого преобразования, `from_chars_result.ec` то параметр имеет тип `errc::result_out_of_range` .

## <a name="requirements"></a>Требования

**Заголовок:**\<charconv>

**Пространство имен:** std

**Параметр компилятора:** /std: c++ 17 или более поздней версии является обязательным

## <a name="see-also"></a>См. также раздел

[from_chars](charconv-functions.md#from_chars)
