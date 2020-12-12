---
description: 'Дополнительные сведения о: to_chars_result struct'
title: Структура to_chars_result
ms.date: 07/22/2020
f1_keywords:
- charconv/std::to_chars_result
helpviewer_keywords:
- to_chars_result class
- to_chars_result structure
ms.openlocfilehash: fb043ba928f086549aea326419ec3a2d673723ba
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97167192"
---
# <a name="to_chars_result-struct"></a>Структура to_chars_result

## <a name="syntax"></a>Синтаксис

```cpp
struct to_chars_result {
    char* ptr;
    errc ec;
};
```

## <a name="members"></a>Члены

|Член|Описание|
|--|--|
|`ptr`| Если `ec` значение равно `errc{}` , преобразование прошло успешно и `ptr` является указателем на один конец записанных символов. В противном случае `ptr` имеет значение `to_chars()` параметра `last` , а содержимое диапазона \[ First (Last)) не указано.|
|`ec` | Код ошибки преобразования. Конкретные коды ошибок см. в разделе [`errc`](system-error-enums.md#errc) .|

## <a name="requirements"></a>Требования

**Заголовок:**\<charconv>

**Пространство имен:** std

**Параметр компилятора:** /std: c++ 17 или более поздней версии является обязательным

## <a name="see-also"></a>См. также раздел

[to_chars](charconv-functions.md#to_chars)
