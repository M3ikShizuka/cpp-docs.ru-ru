---
description: 'Дополнительные сведения о: Ксинкобжект Class'
title: Класс Ксинкобжект
ms.date: 11/04/2016
f1_keywords:
- CSyncObject
- AFXMT/CSyncObject
- AFXMT/CSyncObject::CSyncObject
- AFXMT/CSyncObject::Lock
- AFXMT/CSyncObject::Unlock
- AFXMT/CSyncObject::m_hObject
helpviewer_keywords:
- CSyncObject [MFC], CSyncObject
- CSyncObject [MFC], Lock
- CSyncObject [MFC], Unlock
- CSyncObject [MFC], m_hObject
ms.assetid: c62ea6eb-a17b-4e01-aed4-321fc435a5f4
ms.openlocfilehash: 5743f632f9a8c482ac15995e8d2429851ba015d8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97318602"
---
# <a name="csyncobject-class"></a>Класс Ксинкобжект

Чисто виртуальный класс, обеспечивающий общую функциональность объектов синхронизации Win32.

## <a name="syntax"></a>Синтаксис

```
class CSyncObject : public CObject
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ксинкобжект:: Ксинкобжект](#csyncobject)|Формирует объект `CSyncObject`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ксинкобжект:: Lock](#lock)|Получает доступ к объекту синхронизации.|
|[Ксинкобжект:: Unlock](#unlock)|Получает доступ к объекту синхронизации.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[ОБРАБОТЧИК Ксинкобжект:: operator](#operator_handle)|Предоставляет доступ к объекту синхронизации.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Ксинкобжект:: m_hObject](#m_hobject)|Маркер базового объекта синхронизации.|

## <a name="remarks"></a>Комментарии

Библиотека Microsoft Foundation Class предоставляет несколько классов, производных от `CSyncObject` . Это [цевент](../../mfc/reference/cevent-class.md), [кмутекс](../../mfc/reference/cmutex-class.md), [ккритикалсектион](../../mfc/reference/ccriticalsection-class.md)и [ксемафоре](../../mfc/reference/csemaphore-class.md).

Сведения об использовании объектов синхронизации см. в статье [многопоточность. Использование классов синхронизации](../../parallel/multithreading-how-to-use-the-synchronization-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CSyncObject`

## <a name="requirements"></a>Требования

**Заголовок:** афксмт. h

## <a name="csyncobjectcsyncobject"></a><a name="csyncobject"></a> Ксинкобжект:: Ксинкобжект

Конструирует объект синхронизации с заданным именем.

```
explicit CSyncObject(LPCTSTR pstrName);
virtual ~CSyncObject();
```

### <a name="parameters"></a>Параметры

*пстрнаме*<br/>
Имя объекта. Если значение равно NULL, *пстрнаме* будет иметь значение null.

## <a name="csyncobjectlock"></a><a name="lock"></a> Ксинкобжект:: Lock

Вызовите эту функцию, чтобы получить доступ к ресурсу, управляемому объектом синхронизации.

```
virtual BOOL Lock(DWORD dwTimeout = INFINITE);
```

### <a name="parameters"></a>Параметры

*двтимеаут*<br/>
Указывает время ожидания (сигнала) объекта синхронизации (в миллисекундах). В случае бесконечности `Lock` будет ожидать передачи объекта перед возвратом.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если функция выполнена успешно; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Если объект синхронизации получает сигнал, возвращается значение `Lock` успешно, и поток теперь владеет объектом. Если объект синхронизации несигнальный (недоступен), `Lock` ожидает, пока объект синхронизации получит сигнал о количестве миллисекунд, указанных в параметре *двтимеаут* . Если объект синхронизации не получил сигнал в течение указанного времени, `Lock` возвращает ошибку.

## <a name="csyncobjectm_hobject"></a><a name="m_hobject"></a> Ксинкобжект:: m_hObject

Маркер базового объекта синхронизации.

```
HANDLE m_hObject;
```

## <a name="csyncobjectoperator-handle"></a><a name="operator_handle"></a> ОБРАБОТЧИК Ксинкобжект:: operator

Этот оператор используется для получения маркера `CSyncObject` объекта.

```
operator HANDLE() const;
```

### <a name="return-value"></a>Возвращаемое значение

В случае успеха — маркер объекта синхронизации; в противном случае значение NULL.

### <a name="remarks"></a>Комментарии

Вы можете использовать этот обработчик для непосредственного вызова интерфейсов API Windows.

## <a name="csyncobjectunlock"></a><a name="unlock"></a> Ксинкобжект:: Unlock

Объявление `Unlock` без параметров является чистой виртуальной функцией и должно быть переопределено всеми классами, производными от `CSyncObject` .

```
virtual BOOL Unlock() = 0; virtual BOOL Unlock(
    LONG lCount,
    LPLONG lpPrevCount = NULL);
```

### <a name="parameters"></a>Параметры

*lCount*<br/>
Не используется реализацией по умолчанию.

*лппревкаунт*<br/>
Не используется реализацией по умолчанию.

### <a name="return-value"></a>Возвращаемое значение

Реализация по умолчанию всегда возвращает значение TRUE.

### <a name="remarks"></a>Комментарии

Реализация по умолчанию объявления с двумя параметрами всегда возвращает значение TRUE. Эта функция вызывается для освобождения доступа к объекту синхронизации, принадлежащему вызывающему потоку. Второе объявление предоставляется для объектов синхронизации, таких как семафоры, которые разрешают более одного доступа к контролируемому ресурсу.

## <a name="see-also"></a>См. также раздел

[CObject, класс](../../mfc/reference/cobject-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)
