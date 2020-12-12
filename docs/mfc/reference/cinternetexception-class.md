---
description: 'Дополнительные сведения о: Цинтернетексцептион Class'
title: Класс Цинтернетексцептион
ms.date: 11/04/2016
f1_keywords:
- CInternetException
- AFXINET/CInternetException
- AFXINET/CInternetException::CInternetException
- AFXINET/CInternetException::m_dwContext
- AFXINET/CInternetException::m_dwError
helpviewer_keywords:
- CInternetException [MFC], CInternetException
- CInternetException [MFC], m_dwContext
- CInternetException [MFC], m_dwError
ms.assetid: 44fb3cbe-523e-4754-8843-a77909990b14
ms.openlocfilehash: d46c2eca7f7f568b0296d6ced567d33b49ba4cb6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97209949"
---
# <a name="cinternetexception-class"></a>Класс Цинтернетексцептион

Представляет условие исключения, касающееся интернет-операции.

## <a name="syntax"></a>Синтаксис

```
class CInternetException : public CException
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Цинтернетексцептион:: Цинтернетексцептион](#cinternetexception)|Формирует объект `CInternetException`.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Цинтернетексцептион:: m_dwContext](#m_dwcontext)|Значение контекста, связанное с операцией, вызвавшей исключение.|
|[Цинтернетексцептион:: m_dwError](#m_dwerror)|Ошибка, ставшая причиной исключения.|

## <a name="remarks"></a>Комментарии

`CInternetException`Класс включает два открытых члена данных: один содержит код ошибки, связанный с исключением, а другой — идентификатор контекста Интернет приложения, связанного с ошибкой.

Дополнительные сведения об идентификаторах контекста для Интернет приложений см. в статье [Интернет – программирование с помощью WinInet](../../mfc/win32-internet-extensions-wininet.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CException](../../mfc/reference/cexception-class.md)

`CInternetException`

## <a name="requirements"></a>Требования

**Заголовок:** афксинет. h

## <a name="cinternetexceptioncinternetexception"></a><a name="cinternetexception"></a> Цинтернетексцептион:: Цинтернетексцептион

Эта функция-член вызывается при `CInternetException` создании объекта.

```
CInternetException(DWORD dwError);
```

### <a name="parameters"></a>Параметры

*дверрор*<br/>
Ошибка, ставшая причиной исключения.

### <a name="remarks"></a>Комментарии

Чтобы создать исключение Цинтернетексцептион, вызовите глобальную функцию MFC [афкссровинтернетексцептион](internet-url-parsing-globals.md#afxthrowinternetexception).

## <a name="cinternetexceptionm_dwcontext"></a><a name="m_dwcontext"></a> Цинтернетексцептион:: m_dwContext

Значение контекста, связанное с операцией, связанной с Интернетом.

```
DWORD_PTR m_dwContext;
```

### <a name="remarks"></a>Комментарии

Идентификатор контекста изначально указывается в [Цинтернетсессион](../../mfc/reference/cinternetsession-class.md) и передается из MFC в классы, производные от [Цинтернетконнектион](../../mfc/reference/cinternetconnection-class.md)и [Цинтернетфиле](../../mfc/reference/cinternetfile-class.md). Вы можете переопределить это значение по умолчанию и назначить любой параметр *двконтекст* со значением по своему усмотрению. *двконтекст* связан с любой операцией данного объекта. *двконтекст* определяет сведения о состоянии операции, возвращаемые [Цинтернетсессион:: онстатускаллбакк](../../mfc/reference/cinternetsession-class.md#onstatuscallback).

## <a name="cinternetexceptionm_dwerror"></a><a name="m_dwerror"></a> Цинтернетексцептион:: m_dwError

Ошибка, ставшая причиной исключения.

```
DWORD m_dwError;
```

### <a name="remarks"></a>Комментарии

Это значение ошибки может быть кодом системной ошибки, который находится в файле WINERROR. H или значение ошибки из WININET. H.

Список кодов ошибок Win32 см. в разделе [коды ошибок](/windows/win32/Debug/system-error-codes). Список сообщений об ошибках, связанных с Интернетом, см. в разделе. Оба раздела находятся в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Класс CException](../../mfc/reference/cexception-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс CException](../../mfc/reference/cexception-class.md)
