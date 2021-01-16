---
description: 'Дополнительные сведения о: memcpy, wmemcpy'
title: memcpy, wmemcpy
ms.date: 1/14/2021
api_name:
- memcpy
- wmemcpy
api_location:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- ntoskrnl.exe
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- wmemcpy
- memcpy
helpviewer_keywords:
- wmemcpy function
- memcpy function
ms.assetid: 34abb90b-bffb-46dc-a2f3-a5e9940839d6
ms.openlocfilehash: 49b08877f63bf0d331dcc40e2885b375fe6d1ee7
ms.sourcegitcommit: 1cd8f8a75fd036ffa57bc70f3ca869042d8019d4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "98243142"
---
# <a name="memcpy-wmemcpy"></a>`memcpy`, `wmemcpy`

Копирует байты между буферами. Доступны более безопасные версии этих функций; см. раздел [ `memcpy_s` , `wmemcpy_s` ](memcpy-s-wmemcpy-s.md).

## <a name="syntax"></a>Синтаксис

```C
void *memcpy(
   void *dest,
   const void *src,
   size_t count
);
wchar_t *wmemcpy(
   wchar_t *dest,
   const wchar_t *src,
   size_t count
);
```

### <a name="parameters"></a>Параметры

*`dest`*\
Новый буфер.

*`src`*\
Буфер, из которого происходит копирование.

*`count`*\
Число копируемых символов.

## <a name="return-value"></a>Возвращаемое значение

Значение *`dest`* .

## <a name="remarks"></a>Комментарии

**`memcpy`** копирует *`count`* байт из *`src`* в *`dest`* ; **`wmemcpy`** копирует *`count`* Расширенные символы (два байта). Если источник и назначение перекрываются, поведение **`memcpy`** не определено. Используется **`memmove`** для управления перекрывающимися областями.

> [!IMPORTANT]
> Убедитесь в том, что буфер назначения равен или превосходит по размеру исходный буфер. Дополнительные сведения см. в разделе [Как избежать переполнения буфера](/windows/win32/SecBP/avoiding-buffer-overruns).

> [!IMPORTANT]
> Так как большое количество переполнений буфера и, таким образом, потенциальные эксплойты безопасности, были заблокированы для неправильного использования **`memcpy`** , эта функция перечислена между "запрещенными" функциями жизненного цикла разработки безопасности (SDL).  Можно заметить, что некоторые классы библиотек VC + + продолжают использовать **`memcpy`** .  Кроме того, можно заметить, что оптимизатор компилятора VC + + иногда вызывает метод **`memcpy`** .  Язык Visual C++ разрабатывался в соответствии с требованиями SDL, поэтому использование этой запрещенной функции тщательно анализировалось.  В случае использования в библиотеке вызовы были тщательно изучены на предмет того, не могут ли они вызвать переполнение буфера.  В случае компилятора иногда определенные шаблоны кода распознаются как идентичные шаблону **`memcpy`** и, таким образом, заменяются вызовом функции.  В таких случаях использование метода **`memcpy`** является ненадежным по сравнению с исходными инструкциями. они просто оптимизированы для вызова функции, настроенной с учетом производительности **`memcpy`** .  Точно так же, как использование "безнадежных" функций CRT не гарантирует безопасность (они просто затрудняют их ненадежность), использование "запрещенных" функций не гарантирует опасности (они просто потребовали более тщательного обеспечения безопасности).
>
> Поскольку **`memcpy`** использование в компиляторах VC + + и библиотеках настолько тщательно изучены, эти вызовы разрешены в коде, который в противном случае соответствует SDL.  **`memcpy`** вызовы, представленные в исходном коде приложения, соответствуют требованиям SDL, только если они были проверены экспертами по безопасности.

**`memcpy`** Функции и **`wmemcpy`** будут считаться устаревшими только в том случае, если константа **`_CRT_SECURE_DEPRECATE_MEMORY`** определена перед инструкцией включения, чтобы функции были нерекомендуемыми, например, в примере ниже:

```C
#define _CRT_SECURE_DEPRECATE_MEMORY
#include <memory.h>
```

или

```C
#define _CRT_SECURE_DEPRECATE_MEMORY
#include <wchar.h>
```

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**`memcpy`**|`<memory.h>` или `<string.h>`|
|**`wmemcpy`**|`<wchar.h>`|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

[`memmove`](memmove-wmemmove.md)Пример использования см. в разделе **`memcpy`** .

## <a name="see-also"></a>См. также

[Обработка буфера](../../c-runtime-library/buffer-manipulation.md)\
[`_memccpy`](memccpy.md)\
[`memchr`, `wmemchr`](memchr-wmemchr.md)\
[`memcmp`, `wmemcmp`](memcmp-wmemcmp.md)\
[`memmove`, `wmemmove`](memmove-wmemmove.md)\
[`memset`, `wmemset`](memset-wmemset.md)\
[`strcpy_s`, `wcscpy_s`, `_mbscpy_s`](strcpy-s-wcscpy-s-mbscpy-s.md)\
[`strncpy_s`, `_strncpy_s_l`, `wcsncpy_s`, `_wcsncpy_s_l`, `_mbsncpy_s`, `_mbsncpy_s_l`](strncpy-s-strncpy-s-l-wcsncpy-s-wcsncpy-s-l-mbsncpy-s-mbsncpy-s-l.md)\
