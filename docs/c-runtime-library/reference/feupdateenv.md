---
description: 'Дополнительные сведения о: feupdateenv'
title: feupdateenv
ms.date: 04/05/2018
api_name:
- feupdateenv
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
api_type:
- HeaderDef
f1_keywords:
- feupdateenv
- fenv/feupdateenv
helpviewer_keywords:
- feupdateenv function
ms.assetid: 3d170042-dfd5-4e4f-a55f-038cf2296cc9
ms.openlocfilehash: 4e3fe47c6a03138f2bc82679eb5fc8e938678a17
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97289339"
---
# <a name="feupdateenv"></a>feupdateenv

Сохраняет вызванные в данный момент исключения с плавающей запятой, восстанавливает указанное состояние среды вычислений с плавающей запятой, после чего вызывает сохраненные исключения с плавающей запятой.

## <a name="syntax"></a>Синтаксис

```C
int feupdateenv(
   const fenv_t* penv
);
```

### <a name="parameters"></a>Параметры

*пенв*<br/>
Указатель на объект **fenv_t** , содержащий среду с плавающей запятой, заданную путем вызова [fegetenv](fegetenv1.md) или [feholdexcept](feholdexcept2.md). Кроме того, вы можете указать запускаемую по умолчанию среду вычислений с плавающей запятой с помощью макроса FE_DFL_ENV.

## <a name="return-value"></a>Возвращаемое значение

Если все действия успешно завершены, возвращает 0. В противном случае возвращается ненулевое значение.

## <a name="remarks"></a>Комментарии

Функция **feupdateenv** выполняет несколько действий. Сначала она автоматически сохраняет вызванные на данный момент флаги состояний исключения с плавающей запятой. Затем она устанавливает текущую среду с плавающей запятой из значения, хранящегося в объекте **fenv_t** , на который указывает *пенв*. Если *пенв* не **FE_DFL_ENV** или не указывает на допустимый **fenv_t** объект, последующее поведение не определено. Наконец, **feupdateenv** создает локально хранимые исключения с плавающей точкой.

Чтобы использовать эту функцию, необходимо отключить оптимизацию вычислений с плавающей запятой, которая может препятствовать доступу. Для этого следует использовать директиву `#pragma fenv_access(on)` перед вызовом. Дополнительные сведения см. в разделе [fenv_access](../../preprocessor/fenv-access.md).

## <a name="requirements"></a>Требования

|Функция|Заголовок C|Заголовок C++|
|--------------|--------------|------------------|
|**feupdateenv**|\<fenv.h>|\<cfenv>|

Дополнительные сведения о совместимости см. в статье [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[fegetenv](fegetenv1.md)<br/>
[feclearexcept](feclearexcept1.md)<br/>
[feholdexcept](feholdexcept2.md)<br/>
[fesetexceptflag](fesetexceptflag2.md)<br/>
