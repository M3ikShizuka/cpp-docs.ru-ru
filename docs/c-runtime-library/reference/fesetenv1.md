---
description: 'Дополнительные сведения о: фесетенв'
title: fesetenv
ms.date: 04/05/2018
api_name:
- fesetenv
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
- api-ms-win-crt-runtime-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- fesetenv
- fenv/fesetenv
helpviewer_keywords:
- fesetenv function
ms.assetid: ffc64fff-8ea7-4d59-9e04-ff96ef8cd012
ms.openlocfilehash: 662634e467eb224af813f60ab4434d4857d21d50
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97289443"
---
# <a name="fesetenv"></a>fesetenv

Задает текущую среду с плавающей запятой.

## <a name="syntax"></a>Синтаксис

```C
int fesetenv(
   const fenv_t *penv
);
```

### <a name="parameters"></a>Параметры

*пенв*<br/>
Указатель на объект **fenv_t** , содержащий среду с плавающей запятой, заданную путем вызова [fegetenv](fegetenv1.md) или [feholdexcept](feholdexcept2.md). Можно также указать среду с плавающей запятой по умолчанию при помощи макроса **FE_DFL_ENV** .

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0, если среда был успешно установлена. В противном случае возвращается ненулевое значение.

## <a name="remarks"></a>Комментарии

Функция **фесетенв** устанавливает текущую среду с плавающей запятой из значения, хранящегося в объекте **fenv_t** , на который указывает *пенв*. Среда с плавающей запятой представляет собой набор флагов состояний и режимов управления, влияющих на вычисления с плавающей запятой. Включает режим округления и флаги состояния для исключений с плавающей запятой.  Если *пенв* не **FE_DFL_ENV** или не указывает на допустимый **fenv_t** объект, последующее поведение не определено.

При вызове этой функции устанавливаются флаги состояния исключения, которые находятся в объекте *пенв* , но эти исключения не вызываются.

Чтобы использовать эту функцию, необходимо отключить оптимизацию вычислений с плавающей запятой, которая может препятствовать доступу. Для этого следует использовать директиву `#pragma fenv_access(on)` перед вызовом. Дополнительные сведения см. в разделе [fenv_access](../../preprocessor/fenv-access.md).

## <a name="requirements"></a>Требования

|Функция|Заголовок C|Заголовок C++|
|--------------|--------------|------------------|
|**fesetenv**|\<fenv.h>|\<cfenv>|

Дополнительные сведения о совместимости см. в статье [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Алфавитный справочник по функциям](crt-alphabetical-function-reference.md)<br/>
[fegetenv](fegetenv1.md)<br/>
[feclearexcept](feclearexcept1.md)<br/>
[feholdexcept](feholdexcept2.md)<br/>
[fesetexceptflag](fesetexceptflag2.md)<br/>
