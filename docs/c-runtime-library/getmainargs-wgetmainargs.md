---
description: 'Дополнительные сведения: __getmainargs, __wgetmainargs'
title: __getmainargs, __wgetmainargs
ms.date: 11/04/2016
api_name:
- __wgetmainargs
- __getmainargs
api_location:
- msvcr100.dll
- msvcrt.dll
- msvcr110_clr0400.dll
- msvcr80.dll
- msvcr110.dll
- msvcr90.dll
- msvcr120.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- __wgetmainargs
- __getmainargs
helpviewer_keywords:
- __wgetmainargs
- __getmainargs
ms.assetid: f72f54eb-9509-4bdf-8752-40fc49055439
ms.openlocfilehash: 6f06f83a72d037df6a0973b24ac92ecade6c21eb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97181752"
---
# <a name="__getmainargs-__wgetmainargs"></a>__getmainargs, __wgetmainargs

Вызывает синтаксический анализ командной строки и снова копирует аргументы в `main()` через переданные указатели.

## <a name="syntax"></a>Синтаксис

```cpp
int __getmainargs(
    int * _Argc,
   char *** _Argv,
   char **_ _Env,
   int _DoWildCard,
_startupinfo _ _StartInfo);

int __wgetmainargs (
   int *_Argc,
   wchar_t ***_Argv,
   wchar_t **__Env,
   int _DoWildCard,
   _startupinfo _ _StartInfo)
```

#### <a name="parameters"></a>Параметры

`_Argc`<br/>
Целое число, которое содержит число аргументов, передаваемых в `argv`. Параметр `argc` всегда больше или равен 1.

`_Argv`<br/>
Массив завершающихся null строк, представляющих введенные пользователем программы аргументы командной строки. По соглашению `argv[0]` — это команда, с помощью которой вызывается программа, argv [1] является первым аргументом командной строки и т. д. до argv [argc], которая всегда имеет **значение NULL**. Первый аргумент командной строки — всегда `argv[1]`, а последний — `argv[argc - 1]`.

`_Env`<br/>
Массив строк, которые представляют переменные, заданные в среде пользователя. Этот массив завершается записью **со значением NULL** .

`_DoWildCard`<br/>
Целое число, которое, если имеет значение 1, разворачивает подстановочные знаки в аргументах командной строки, а если имеет значение 0, не выполняет никаких действий.

`_StartInfo`<br/>
Другие сведения, передаваемые в DLL CRT.

## <a name="return-value"></a>Возвращаемое значение

0 в случае успешного выполнения; отрицательное значение, если операция завершилась неудачей.

## <a name="remarks"></a>Комментарии

Используйте `__getmainargs` на платформах без расширенных символов и `__wgetmainargs` на платформах расширенных символов (Unicode).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|__getmainargs|internal.h|
|__wgetmainargs|internal.h|
