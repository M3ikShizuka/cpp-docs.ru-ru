---
description: 'Дополнительные сведения: _set_app_type'
title: _set_app_type
ms.date: 4/2/2020
api_name:
- _set_app_type
- _o__set_app_type
api_location:
- api-ms-win-crt-runtime-l1-1-0.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _set_app_type
- corecrt_startup/_set_app_type
ms.assetid: 1e7fe786-b587-4116-8c05-f7d762350100
ms.openlocfilehash: cd04f1c17f7876c08f8eafb4ef77960073fb3f33
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97277106"
---
# <a name="_set_app_type"></a>_set_app_type

Внутренняя функция используется при запуске для того, чтобы сообщить CRT, является ли приложение консольным приложением или приложением с графическим интерфейсом.

## <a name="syntax"></a>Синтаксис

```cpp
typedef enum _crt_app_type
{
    _crt_unknown_app,
    _crt_console_app,
    _crt_gui_app
} _crt_app_type;

void __cdecl _set_app_type(
    _crt_app_type appType
    );
```

## <a name="parameters"></a>Параметры

*appType*<br/>
Значение, указывающее на тип приложения. Допустимые значения:

|Значение|Описание|
|----------------|-----------------|
|_crt_unknown_app|Неизвестный тип приложения.|
|_crt_console_app|Приложение консоли (командной строки).|
|_crt_gui_app|Приложение с графическим интерфейсом (Windows).|

## <a name="remarks"></a>Комментарии

Обычно вызывать эту функцию не нужно. Она входит в код запуска среды выполнения C, который выполняется перед вызовом `main` в приложении.

По умолчанию глобальное состояние этой функции ограничивается приложением. Чтобы изменить это, см. раздел [глобальное состояние в CRT](global-state.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|_set_app_type|process.h|
