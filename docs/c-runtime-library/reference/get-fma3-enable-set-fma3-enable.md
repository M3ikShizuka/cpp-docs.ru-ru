---
description: 'Дополнительные сведения: _get_FMA3_enable, _set_FMA3_enable'
title: _get_FMA3_enable, _set_FMA3_enable
ms.date: 1/14/2021
api_name:
- _get_FMA3_enable
- _set_FMA3_enable
api_location:
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-runtime-l1-1-0.dll
- api-ms-win-crt-math-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _get_FMA3_enable
- _set_FMA3_enable
- math/_get_FMA3_enable
- math/_set_FMA3_enable
helpviewer_keywords:
- _get_FMA3_enable
- _set_FMA3_enable
ms.assetid: 4c1dc4bc-e86b-451b-9211-5a2ba6c98ee4
ms.openlocfilehash: 48c70185b73c2f7bb05677fdb550c2c0535d8992
ms.sourcegitcommit: 1cd8f8a75fd036ffa57bc70f3ca869042d8019d4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "98243090"
---
# <a name="_get_fma3_enable-_set_fma3_enable"></a>_get_FMA3_enable, _set_FMA3_enable

Возвращает или задает флаг, указывающий, используют ли трансцендентных математические функции библиотеки с плавающей запятой инструкции FMA3 в коде, скомпилированном для платформ x64.

## <a name="syntax"></a>Синтаксис

```C
int _set_FMA3_enable(int flag);
int _get_FMA3_enable();
```

### <a name="parameters"></a>Параметры

*flag*<br/>
Задайте значение 1, чтобы включить реализации FMA3 функций трансцендентных математическими функциями библиотеки с плавающей запятой на платформах x64 или 0 для использования реализаций, которые не используют инструкции FMA3.

## <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если включены реализации FMA3 трансцендентных математических функций библиотеки с плавающей запятой. В противном случае — нуль.

## <a name="remarks"></a>Комментарии

Используйте функцию **_set_FMA3_enable** , чтобы включить или отключить использование инструкций FMA3 в трансцендентных математических функциях с плавающей запятой в библиотеке CRT. Возвращаемое значение отражает реализацию, используемую после изменения. Если ЦП не поддерживает инструкции FMA3, эта функция не может включить их в библиотеке, а возвращаемое значение равно нулю. Используйте **_get_FMA3_enable** , чтобы получить текущее состояние библиотеки. По умолчанию на платформах x64 код запуска CRT определяет, поддерживает ли ЦП инструкции FMA3, а также включает или отключает реализации FMA3 в библиотеке.

Поскольку реализации FMA3 используют разные алгоритмы, незначительные различия в результатах вычислений могут быть наблюдаемыми при включении или отключении реализаций FMA3 или между компьютерами, которые не поддерживают FMA3. Дополнительные сведения см. в статье [проблемы при миграции с плавающей запятой](../../porting/floating-point-migration-issues.md).

## <a name="requirements"></a>Требования

Функции **_set_FMA3_enable** и **_get_FMA3_enable** доступны только в 64-разрядных версиях CRT.

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**_set_FMA3_enable**, **_get_FMA3_enable**| Ц \<math.h><br />C++: \<cmath> или \<math.h>|

Функции **_set_FMA3_enable** и **_get_FMA3_enable** являются специфичными для Microsoft. Сведения о совместимости см. в разделе [Совместимость](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также

[Поддержка чисел с плавающей запятой](../../c-runtime-library/floating-point-support.md)<br/>
[Проблемы при миграции с плавающей запятой](../../porting/floating-point-migration-issues.md)<br/>
