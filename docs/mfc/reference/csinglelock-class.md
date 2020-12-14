---
description: 'Дополнительные сведения о: Ксинглелокк Class'
title: Класс Ксинглелокк
ms.date: 11/04/2016
f1_keywords:
- CSingleLock
- AFXMT/CSingleLock
- AFXMT/CSingleLock::CSingleLock
- AFXMT/CSingleLock::IsLocked
- AFXMT/CSingleLock::Lock
- AFXMT/CSingleLock::Unlock
helpviewer_keywords:
- CSingleLock [MFC], CSingleLock
- CSingleLock [MFC], IsLocked
- CSingleLock [MFC], Lock
- CSingleLock [MFC], Unlock
ms.assetid: 7dae7288-8066-4a3e-85e0-78d28bfc6bc8
ms.openlocfilehash: 7fa4fe32ce38bf47ede1b6ac133d1a057907f9c2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97342860"
---
# <a name="csinglelock-class"></a>Класс Ксинглелокк

Класс представляет механизм контроля доступа к определенному ресурсу в многопоточных программах.

## <a name="syntax"></a>Синтаксис

```
class CSingleLock
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ксинглелокк:: Ксинглелокк](#csinglelock)|Формирует объект `CSingleLock`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ксинглелокк:: NOLOCK](#islocked)|Определяет, заблокирован ли объект.|
|[Ксинглелокк:: Lock](#lock)|Ожидает объект синхронизации.|
|[Ксинглелокк:: Unlock](#unlock)|Освобождает объект синхронизации.|

## <a name="remarks"></a>Комментарии

`CSingleLock` не имеет базового класса.

Чтобы использовать классы синхронизации [ксемафоре](../../mfc/reference/csemaphore-class.md), [кмутекс](../../mfc/reference/cmutex-class.md), [ккритикалсектион](../../mfc/reference/ccriticalsection-class.md)и [Цевент](../../mfc/reference/cevent-class.md), необходимо создать либо `CSingleLock` объект или [кмултилокк](../../mfc/reference/cmultilock-class.md) , чтобы дождаться и освободить объект синхронизации. Используйте `CSingleLock` , когда требуется только один объект за раз. Используется `CMultiLock` при наличии нескольких объектов, которые можно использовать в определенный момент времени.

Чтобы использовать `CSingleLock` объект, вызовите его конструктор внутри функции-члена в классе контролируемого ресурса. Затем вызовите функцию-член [NOLOCK](#islocked) , чтобы определить, доступен ли ресурс. Если это так, продолжайте работу с оставшейся частью функции-члена. Если ресурс недоступен, подождите указанное количество времени для освобождения ресурса или возвратите ошибку. После завершения использования ресурса либо вызовите функцию [Unlock](#unlock) , если `CSingleLock` объект будет использоваться повторно, либо разрешите `CSingleLock` уничтожение объекта.

`CSingleLock` для объектов требуется наличие объекта, производного от [ксинкобжект](../../mfc/reference/csyncobject-class.md). Обычно это элемент данных класса контролируемого ресурса. Дополнительные сведения об использовании `CSingleLock` объектов см. в статье [многопоточность. Использование классов синхронизации](../../parallel/multithreading-how-to-use-the-synchronization-classes.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CSingleLock`

## <a name="requirements"></a>Требования

**Заголовок:** афксмт. h

## <a name="csinglelockcsinglelock"></a><a name="csinglelock"></a> Ксинглелокк:: Ксинглелокк

Формирует объект `CSingleLock`.

```
explicit CSingleLock(
    CSyncObject* pObject,
    BOOL bInitialLock = FALSE);
```

### <a name="parameters"></a>Параметры

*Объект*<br/>
Указывает на объект синхронизации, к которому будет осуществляться доступ. Не может быть NULL.

*бинитиаллокк*<br/>
Указывает, следует ли первоначально пытаться получить доступ к указанному объекту.

### <a name="remarks"></a>Комментарии

Эта функция обычно вызывается из функции-члена доступа контролируемого ресурса.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFC_Utilities#19](../../mfc/codesnippet/cpp/csinglelock-class_1.h)]

## <a name="csinglelockislocked"></a><a name="islocked"></a> Ксинглелокк:: NOLOCK

Определяет, является ли объект, связанный с `CSingleLock` объектом, несигнальным (недоступным).

```
BOOL IsLocked();
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если объект заблокирован; в противном случае — 0.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFC_Utilities#20](../../mfc/codesnippet/cpp/csinglelock-class_2.h)]

## <a name="csinglelocklock"></a><a name="lock"></a> Ксинглелокк:: Lock

Вызовите эту функцию, чтобы получить доступ к ресурсу, управляемому объектом синхронизации, предоставленному `CSingleLock` конструктору.

```
BOOL Lock(DWORD dwTimeOut = INFINITE);
```

### <a name="parameters"></a>Параметры

*двтимеаут*<br/>
Указывает период времени ожидания доступности объекта синхронизации (сигнальный). В случае бесконечности `Lock` будет ожидать передачи объекта перед возвратом.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если функция выполнена успешно; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Если объект синхронизации получает сигнал, возвращается значение `Lock` успешно, и поток теперь владеет объектом. Если объект синхронизации несигнальный (недоступен), `Lock` ожидает, пока объект синхронизации получит сигнал о количестве миллисекунд, указанных в параметре *двтимеаут* . Если объект синхронизации не получил сигнал в течение указанного времени, `Lock` возвращает ошибку.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFC_Utilities#21](../../mfc/codesnippet/cpp/csinglelock-class_3.h)]

## <a name="csinglelockunlock"></a><a name="unlock"></a> Ксинглелокк:: Unlock

Освобождает объект синхронизации, принадлежащий `CSingleLock` .

```
BOOL Unlock();

BOOL Unlock(
    LONG lCount,
    LPLONG lPrevCount = NULL);
```

### <a name="parameters"></a>Параметры

*lCount*<br/>
Число обращений к выпуску. Должно быть больше 0. Если указанный объем приведет к превышению максимального значения счетчика объекта, счетчик не изменится и функция вернет значение FALSE.

*лпревкаунт*<br/>
Указывает на переменную для получения предыдущего счетчика объекта синхронизации. Если значение равно NULL, то предыдущее число не возвращается.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если функция выполнена успешно; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Эта функция вызывается `CSingleLock` деструктором.

Если необходимо освободить несколько счетчиков доступа для семафора, используйте вторую форму `Unlock` и укажите количество обращений к выпуску.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFC_Utilities#21](../../mfc/codesnippet/cpp/csinglelock-class_3.h)]

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Кмултилокк](../../mfc/reference/cmultilock-class.md)
