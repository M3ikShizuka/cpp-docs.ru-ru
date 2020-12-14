---
description: 'Дополнительные сведения: _amsg_exit'
title: _amsg_exit
ms.date: 11/04/2016
api_name:
- _amsg_exit
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
- DLLExport
topic_type:
- apiref
f1_keywords:
- _amsg_exit
helpviewer_keywords:
- _amsg_exit
ms.assetid: 146d4faf-d763-43a4-b264-12711196456b
ms.openlocfilehash: d00283f3222a217db8337129f66b377f7c0d494e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97211405"
---
# <a name="_amsg_exit"></a>_amsg_exit

Создает указанное сообщение об ошибке времени выполнения, затем завершает приложение с кодом ошибки 255.

## <a name="syntax"></a>Синтаксис

```cpp
void _amsg_exit ( int rterrnum );
```

### <a name="parameters"></a>Параметры

*ртеррнум*<br/>
Идентификационный номер определяемого системой сообщения об ошибке времени выполнения.

## <a name="remarks"></a>Комментарии

Эта функция посылает сообщение об ошибке времени выполнения в поток **stderr** для консольных приложений или отображает сообщение в окне сообщения для приложений Windows. В режиме отладки перед выходом можно вызвать отладчик.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|_amsg_exit|internal.h|
