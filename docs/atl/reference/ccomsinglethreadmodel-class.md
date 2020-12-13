---
description: 'Дополнительные сведения о: Ккомсинглесреадмодел Class'
title: Класс Ккомсинглесреадмодел
ms.date: 2/29/2020
f1_keywords:
- CComSingleThreadModel
- ATLBASE/ATL::CComSingleThreadModel
- ATLBASE/ATL::CComSingleThreadModel::AutoCriticalSection
- ATLBASE/ATL::CComSingleThreadModel::CriticalSection
- ATLBASE/ATL::CComSingleThreadModel::ThreadModelNoCS
- ATLBASE/ATL::CComSingleThreadModel::Decrement
- ATLBASE/ATL::CComSingleThreadModel::Increment
helpviewer_keywords:
- single-threaded applications
- CComSingleThreadModel class
- single-threaded applications, ATL
ms.assetid: e5dc30c7-405a-4ba4-8ae9-51937243fce8
ms.openlocfilehash: 42f1111590dd8e03a541ecc7a71b461e34a08f0b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142211"
---
# <a name="ccomsinglethreadmodel-class"></a>Класс Ккомсинглесреадмодел

Этот класс предоставляет методы для увеличения и уменьшения значения переменной.

## <a name="syntax"></a>Синтаксис

```
class CComSingleThreadModel
```

## <a name="members"></a>Члены

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|[Ккомсинглесреадмодел:: Аутокритикалсектион](#autocriticalsection)|Ссылается на класс [ккомфакекритикалсектион](../../atl/reference/ccomfakecriticalsection-class.md).|
|[Ккомсинглесреадмодел:: CriticalSection](#criticalsection)|Ссылка на класс `CComFakeCriticalSection` .|
|[Ккомсинглесреадмодел:: Среадмоделнокс](#threadmodelnocs)|Ссылки `CComSingleThreadModel` .|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккомсинглесреадмодел::D екремент](#decrement)|Уменьшает значение указанной переменной. Эта реализация не является потокобезопасной.|
|[Ккомсинглесреадмодел:: Increment](#increment)|Увеличивает значение указанной переменной. Эта реализация не является потокобезопасной.|

## <a name="remarks"></a>Комментарии

`CComSingleThreadModel` предоставляет методы для увеличения и уменьшения значения переменной. В отличие от [ккоммултисреадмодел](../../atl/reference/ccommultithreadmodel-class.md) и [ккоммултисреадмоделнокс](../../atl/reference/ccommultithreadmodelnocs-class.md), эти методы не являются потокобезопасными.

Обычно используется `CComSingleThreadModel` одно из двух **`typedef`** имен: [ккомобжектсреадмодел](atl-typedefs.md#ccomobjectthreadmodel) или [ккомглобалссреадмодел](atl-typedefs.md#ccomglobalsthreadmodel). Класс, на который ссылается каждый, **`typedef`** зависит от используемой потоковой модели, как показано в следующей таблице.

|typedef|Модель с одним потоком|Потоковая модель потоков|Модель свободной потоковой модели|
|-------------|----------------------------|-------------------------------|--------------------------|
|`CComObjectThreadModel`|S|S|M|
|`CComGlobalsThreadModel`|S|M|M|

S = `CComSingleThreadModel` ; M = `CComMultiThreadModel`

`CComSingleThreadModel` сам определяет три **`typedef`** имени. `ThreadModelNoCS` ссылки `CComSingleThreadModel` . `AutoCriticalSection` и `CriticalSection` ссылочный класс [ккомфакекритикалсектион](../../atl/reference/ccomfakecriticalsection-class.md), предоставляющий пустые методы, связанные с получением и освобождением владения критическим разделом.

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="ccomsinglethreadmodelautocriticalsection"></a><a name="autocriticalsection"></a> Ккомсинглесреадмодел:: Аутокритикалсектион

При использовании `CComSingleThreadModel` **`typedef`** имя `AutoCriticalSection` ссылается на класс [ккомфакекритикалсектион](../../atl/reference/ccomfakecriticalsection-class.md).

```
typedef CComFakeCriticalSection AutoCriticalSection;
```

### <a name="remarks"></a>Комментарии

Поскольку не `CComFakeCriticalSection` предоставляет критическую секцию, его методы не выполняют никаких действий.

[Ккоммултисреадмодел](../../atl/reference/ccommultithreadmodel-class.md) и [ккоммултисреадмоделнокс](../../atl/reference/ccommultithreadmodelnocs-class.md) содержат определения для `AutoCriticalSection` . В следующей таблице показана связь между классом потоковой модели и классом критического раздела, на который ссылается `AutoCriticalSection` :

|Класс, определенный в|Ссылка на класс|
|----------------------|----------------------|
|`CComSingleThreadModel`|`CComFakeCriticalSection`|
|`CComMultiThreadModel`|`CComAutoCriticalSection`|
|`CComMultiThreadModelNoCS`|`CComFakeCriticalSection`|

Кроме того `AutoCriticalSection` , можно использовать **`typedef`** имя [CriticalSection](#criticalsection). Не следует указывать `AutoCriticalSection` в глобальных объектах или членах статических классов, если требуется исключить код запуска CRT.

### <a name="example"></a>Пример

См. раздел [ккоммултисреадмодел:: аутокритикалсектион](../../atl/reference/ccommultithreadmodel-class.md#autocriticalsection).

## <a name="ccomsinglethreadmodelcriticalsection"></a><a name="criticalsection"></a> Ккомсинглесреадмодел:: CriticalSection

При использовании `CComSingleThreadModel` **`typedef`** имя `CriticalSection` ссылается на класс [ккомфакекритикалсектион](../../atl/reference/ccomfakecriticalsection-class.md).

```
typedef CComFakeCriticalSection CriticalSection;
```

### <a name="remarks"></a>Комментарии

Поскольку не `CComFakeCriticalSection` предоставляет критическую секцию, его методы не выполняют никаких действий.

[Ккоммултисреадмодел](../../atl/reference/ccommultithreadmodel-class.md) и [ккоммултисреадмоделнокс](../../atl/reference/ccommultithreadmodelnocs-class.md) содержат определения для `CriticalSection` . В следующей таблице показана связь между классом потоковой модели и классом критического раздела, на который ссылается `CriticalSection` :

|Класс, определенный в|Ссылка на класс|
|----------------------|----------------------|
|`CComSingleThreadModel`|`CComFakeCriticalSection`|
|`CComMultiThreadModel`|`CComCriticalSection`|
|`CComMultiThreadModelNoCS`|`CComFakeCriticalSection`|

Кроме того `CriticalSection` , можно использовать **`typedef`** имя [аутокритикалсектион](#autocriticalsection). Не следует указывать `AutoCriticalSection` в глобальных объектах или членах статических классов, если требуется исключить код запуска CRT.

### <a name="example"></a>Пример

См. раздел [ккоммултисреадмодел:: аутокритикалсектион](../../atl/reference/ccommultithreadmodel-class.md#autocriticalsection).

## <a name="ccomsinglethreadmodeldecrement"></a><a name="decrement"></a> Ккомсинглесреадмодел::D екремент

Эта статическая функция уменьшает значение переменной, на которую указывает *p*.

```
static ULONG WINAPI Decrement(LPLONG p) throw();
```

### <a name="parameters"></a>Параметры

*p*<br/>
окне Указатель на переменную, которую необходимо уменьшить.

### <a name="return-value"></a>Возвращаемое значение

Результат декремента.

## <a name="ccomsinglethreadmodelincrement"></a><a name="increment"></a> Ккомсинглесреадмодел:: Increment

Эта статическая функция увеличивает значение переменной, на которую указывает *p*.

```
static ULONG WINAPI Increment(LPLONG p) throw();
```

### <a name="parameters"></a>Параметры

*p*<br/>
окне Указатель на переменную, которая должна быть увеличена.

### <a name="return-value"></a>Возвращаемое значение

Результат приращения.

## <a name="ccomsinglethreadmodelthreadmodelnocs"></a><a name="threadmodelnocs"></a> Ккомсинглесреадмодел:: Среадмоделнокс

При использовании `CComSingleThreadModel` **`typedef`** имя `ThreadModelNoCS` просто ссылается на `CComSingleThreadModel` .

```
typedef CComSingleThreadModel ThreadModelNoCS;
```

### <a name="remarks"></a>Комментарии

[Ккоммултисреадмодел](../../atl/reference/ccommultithreadmodel-class.md) и [ккоммултисреадмоделнокс](../../atl/reference/ccommultithreadmodelnocs-class.md) содержат определения для `ThreadModelNoCS` . В следующей таблице показана связь между классом потоковой модели и классом, на который ссылается `ThreadModelNoCS` :

|Класс, определенный в|Ссылка на класс|
|----------------------|----------------------|
|`CComSingleThreadModel`|`CComSingleThreadModel`|
|`CComMultiThreadModel`|`CComMultiThreadModelNoCS`|
|`CComMultiThreadModelNoCS`|`CComMultiThreadModelNoCS`|

### <a name="example"></a>Пример

См. раздел [ккоммултисреадмодел:: аутокритикалсектион](../../atl/reference/ccommultithreadmodel-class.md#autocriticalsection).

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
