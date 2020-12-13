---
description: 'Дополнительные сведения о: Кртсреадтраитс Class'
title: Класс Кртсреадтраитс
ms.date: 11/04/2016
f1_keywords:
- CRTThreadTraits
- ATLBASE/ATL::CRTThreadTraits
- ATLBASE/ATL::CRTThreadTraits::CreateThread
helpviewer_keywords:
- CRTThreadTraits class
- threading [ATL], creation functions
- threading [ATL], CRT threads
ms.assetid: eb6e20b0-c2aa-4170-8e34-aaeeacc86343
ms.openlocfilehash: 30f9f435ad447a33d513379ceee0d254f48dfec8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97140846"
---
# <a name="crtthreadtraits-class"></a>Класс Кртсреадтраитс

Этот класс предоставляет функцию создания для потока CRT. Используйте этот класс, если поток будет использовать функции CRT.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
class CRTThreadTraits
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кртсреадтраитс:: CreateThread](#createthread)|Статически Вызовите эту функцию, чтобы создать поток, который может использовать функции CRT.|

## <a name="remarks"></a>Комментарии

Признаки потоков — это классы, которые предоставляют функцию создания для определенного типа потока. Функция создания имеет ту же сигнатуру и семантику, что и функция Windows [CreateThread](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) .

Признаки потоков используются в следующих классах:

- [CThreadPool](../../atl/reference/cthreadpool-class.md)

- [кворкерсреад](../../atl/reference/cworkerthread-class.md)

Если поток не будет использовать функции CRT, используйте вместо него [Win32ThreadTraits](../../atl/reference/win32threadtraits-class.md) .

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="crtthreadtraitscreatethread"></a><a name="createthread"></a> Кртсреадтраитс:: CreateThread

Вызовите эту функцию, чтобы создать поток, который может использовать функции CRT.

```
static HANDLE CreateThread(
    LPSECURITY_ATTRIBUTES lpsa,
    DWORD dwStackSize,
    LPTHREAD_START_ROUTINE pfnThreadProc,
    void* pvParam,
    DWORD dwCreationFlags,
    DWORD* pdwThreadId) throw();
```

### <a name="parameters"></a>Параметры

*лпса*<br/>
Атрибуты безопасности для нового потока.

*двстакксизе*<br/>
Размер стека для нового потока.

*пфнсреадпрок*<br/>
Потоковая процедура нового потока.

*пвпарам*<br/>
Параметр, передаваемый в процедуру потока.

*двкреатионфлагс*<br/>
Флаги создания (0 или CREATE_SUSPENDED).

*пдвсреадид*<br/>
заполняет Адрес переменной типа DWORD, которая в случае успешного выполнения получает идентификатор созданного потока.

### <a name="return-value"></a>Возвращаемое значение

Возвращает маркер вновь созданного потока или значение NULL при сбое. Вызовите [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить расширенные сведения об ошибке.

### <a name="remarks"></a>Комментарии

Дополнительные сведения о параметрах этой функции см. в разделе [CreateThread](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) .

Эта функция вызывает [_beginthreadex](../../c-runtime-library/reference/beginthread-beginthreadex.md) , чтобы создать поток.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
