---
description: 'Дополнительные сведения о: srand'
title: srand
ms.date: 4/2/2020
api_name:
- srand
- _o_srand
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
- api-ms-win-crt-utility-l1-1-0.dll
- ntoskrnl.exe
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- srand
helpviewer_keywords:
- random starting point
- random starting point, setting
- random numbers, generating
- srand function
- numbers, pseudorandom
- numbers, random
- pseudorandom numbers
- starting points, setting random
- starting points
ms.openlocfilehash: bea91841b549fae09faa4345767fc22cf4d6208e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97292174"
---
# <a name="srand"></a>srand

Задает начальное начальное значение для генератора номеров псевдослучайное, используемого функцией **Rand** .

## <a name="syntax"></a>Синтаксис

```C
void srand(
   unsigned int seed
);
```

### <a name="parameters"></a>Параметры

*seed*<br/>
Начальное значение для создания псевдослучайных чисел

## <a name="remarks"></a>Комментарии

Функция **srand** задает начальную точку для создания последовательности целых чисел псевдослучайное в текущем потоке. Чтобы повторно инициализировать генератор для создания той же последовательности результатов, вызовите функцию **srand** и снова используйте один и тот же аргумент *начального значения* . Любое другое значение *начального* значения задает генератору другую начальную точку в последовательности псевдослучайное. **Rand** извлекает созданные номера псевдослучайное. Вызов **функции RAND** перед любым вызовом **srand** создает ту же последовательность, что и вызов **srand** с *начальным* значением, переданным как 1.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](../global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**srand**|\<stdlib.h>|

Дополнительные сведения о совместимости см. в статье [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

См. пример для [rand](rand.md).

## <a name="see-also"></a>См. также раздел

[Поддержка операций с плавающей запятой](../../c-runtime-library/floating-point-support.md)<br/>
[rand](rand.md)<br/>
