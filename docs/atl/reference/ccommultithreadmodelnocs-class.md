---
description: 'Дополнительные сведения о: Ккоммултисреадмоделнокс Class'
title: Класс Ккоммултисреадмоделнокс
ms.date: 11/04/2016
f1_keywords:
- CComMultiThreadModelNoCS
- ATLBASE/ATL::CComMultiThreadModelNoCS
- ATLBASE/ATL::CComMultiThreadModelNoCS::AutoCriticalSection
- ATLBASE/ATL::CComMultiThreadModelNoCS::CriticalSection
- ATLBASE/ATL::CComMultiThreadModelNoCS::ThreadModelNoCS
- ATLBASE/ATL::CComMultiThreadModelNoCS::Decrement
- ATLBASE/ATL::CComMultiThreadModelNoCS::Increment
helpviewer_keywords:
- ATL, multithreading
- CComMultiThreadModelNoCS class
- threading [ATL]
ms.assetid: 2b3f7a45-fd72-452c-aaf3-ccdaa621c821
ms.openlocfilehash: 8b26c59564f9a7869bb3429ee31284925815e6ac
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97152013"
---
# <a name="ccommultithreadmodelnocs-class"></a>Класс Ккоммултисреадмоделнокс

`CComMultiThreadModelNoCS` предоставляет потокобезопасные методы для увеличения и уменьшения значения переменной без блокировки критической секции или разблокировки.

## <a name="syntax"></a>Синтаксис

```
class CComMultiThreadModelNoCS
```

## <a name="members"></a>Члены

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|[Ккоммултисреадмоделнокс:: Аутокритикалсектион](#autocriticalsection)|Ссылается на класс [ккомфакекритикалсектион](../../atl/reference/ccomfakecriticalsection-class.md).|
|[Ккоммултисреадмоделнокс:: CriticalSection](#criticalsection)|Ссылка на класс `CComFakeCriticalSection` .|
|[Ккоммултисреадмоделнокс:: Среадмоделнокс](#threadmodelnocs)|Ссылка на класс `CComMultiThreadModelNoCS` .|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккоммултисреадмоделнокс::D екремент](#decrement)|Статически Уменьшает значение указанной переменной в безопасном для потоков режиме.|
|[Ккоммултисреадмоделнокс:: Increment](#increment)|Статически Увеличивает значение указанной переменной в безопасном для потоков режиме.|

## <a name="remarks"></a>Комментарии

`CComMultiThreadModelNoCS` аналогичен [ккоммултисреадмодел](../../atl/reference/ccommultithreadmodel-class.md) в том, что он предоставляет потокобезопасные методы для увеличения и уменьшения переменной. Однако при ссылке на класс критической секции с помощью `CComMultiThreadModelNoCS` методы, такие как `Lock` и, `Unlock` не будут выполнять никаких действий.

Обычно используется `CComMultiThreadModelNoCS` `ThreadModelNoCS` **`typedef`** имя. Это **`typedef`** определяется в `CComMultiThreadModelNoCS` , `CComMultiThreadModel` и [ккомсинглесреадмодел](../../atl/reference/ccomsinglethreadmodel-class.md).

> [!NOTE]
> Глобальные **`typedef`** имена [Ккомобжектсреадмодел](atl-typedefs.md#ccomobjectthreadmodel) и [ккомглобалссреадмодел](atl-typedefs.md#ccomglobalsthreadmodel) не ссылаются `CComMultiThreadModelNoCS` .

В дополнение к `ThreadModelNoCS` , `CComMultiThreadModelNoCS` определяет `AutoCriticalSection` и `CriticalSection` . Эти два последних **`typedef`** имени ссылаются на [ккомфакекритикалсектион](../../atl/reference/ccomfakecriticalsection-class.md), которые предоставляют пустые методы, связанные с получением и освобождением критической секции.

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="ccommultithreadmodelnocsautocriticalsection"></a><a name="autocriticalsection"></a> Ккоммултисреадмоделнокс:: Аутокритикалсектион

При использовании `CComMultiThreadModelNoCS` **`typedef`** имя `AutoCriticalSection` ссылается на класс [ккомфакекритикалсектион](../../atl/reference/ccomfakecriticalsection-class.md).

```
typedef CComFakeCriticalSection AutoCriticalSection;
```

### <a name="remarks"></a>Комментарии

Поскольку не `CComFakeCriticalSection` предоставляет критическую секцию, его методы не выполняют никаких действий.

[Ккоммултисреадмодел](../../atl/reference/ccommultithreadmodel-class.md) и [ккомсинглесреадмодел](../../atl/reference/ccomsinglethreadmodel-class.md) также содержат определения для `AutoCriticalSection` . В следующей таблице показана связь между классом потоковой модели и классом критического раздела, на который ссылается `AutoCriticalSection` :

|Класс, определенный в|Ссылка на класс|
|----------------------|----------------------|
|`CComMultiThreadModelNoCS`|`CComFakeCriticalSection`|
|`CComMultiThreadModel`|`CComAutoCriticalSection`|
|`CComSingleThreadModel`|`CComFakeCriticalSection`|

Кроме того `AutoCriticalSection` , можно использовать **`typedef`** имя [CriticalSection](#criticalsection). Не следует указывать `AutoCriticalSection` в глобальных объектах или членах статических классов, если требуется исключить код запуска CRT.

### <a name="example"></a>Пример

См. раздел [ккоммултисреадмодел:: аутокритикалсектион](../../atl/reference/ccommultithreadmodel-class.md#autocriticalsection).

## <a name="ccommultithreadmodelnocscriticalsection"></a><a name="criticalsection"></a> Ккоммултисреадмоделнокс:: CriticalSection

При использовании `CComMultiThreadModelNoCS` **`typedef`** имя `CriticalSection` ссылается на класс [ккомфакекритикалсектион](../../atl/reference/ccomfakecriticalsection-class.md).

```
typedef CComFakeCriticalSection CriticalSection;
```

### <a name="remarks"></a>Комментарии

Поскольку не `CComFakeCriticalSection` предоставляет критическую секцию, его методы не выполняют никаких действий.

[Ккоммултисреадмодел](../../atl/reference/ccommultithreadmodel-class.md) и [ккомсинглесреадмодел](../../atl/reference/ccomsinglethreadmodel-class.md) также содержат определения для `CriticalSection` . В следующей таблице показана связь между классом потоковой модели и классом критического раздела, на который ссылается `CriticalSection` :

|Класс, определенный в|Ссылка на класс|
|----------------------|----------------------|
|`CComMultiThreadModelNoCS`|`CComFakeCriticalSection`|
|`CComMultiThreadModel`|`CComCriticalSection`|
|`CComSingleThreadModel`|`CComFakeCriticalSection`|

Кроме того `CriticalSection` , можно использовать **`typedef`** имя `AutoCriticalSection` . Не следует указывать `AutoCriticalSection` в глобальных объектах или членах статических классов, если требуется исключить код запуска CRT.

### <a name="example"></a>Пример

См. раздел [ккоммултисреадмодел:: аутокритикалсектион](../../atl/reference/ccommultithreadmodel-class.md#autocriticalsection).

## <a name="ccommultithreadmodelnocsdecrement"></a><a name="decrement"></a> Ккоммултисреадмоделнокс::D екремент

Эта статическая функция вызывает функцию Win32 [интерлоккеддекремент](/windows/win32/api/winnt/nf-winnt-interlockeddecrement), которая уменьшает значение переменной, на которую указывает *p*.

```
static ULONG WINAPI Decrement(LPLONG p) throw();
```

### <a name="parameters"></a>Параметры

*p*<br/>
окне Указатель на переменную, которую необходимо уменьшить.

### <a name="return-value"></a>Возвращаемое значение

Если результат декремента равен 0, то `Decrement` возвращает 0. Если результат декремента равен нулю, то возвращаемое значение также является ненулевым, но может не совпадать с результатом декремента.

### <a name="remarks"></a>Комментарии

**Интерлоккеддекремент** предотвращает одновременное использование этой переменной более чем одним потоком.

## <a name="ccommultithreadmodelnocsincrement"></a><a name="increment"></a> Ккоммултисреадмоделнокс:: Increment

Эта статическая функция вызывает функцию Win32 [интерлоккединкремент](/windows/win32/api/winnt/nf-winnt-interlockedincrement), которая увеличивает значение переменной, на которую указывает *p*.

```
static ULONG WINAPI Increment(LPLONG p) throw();
```

### <a name="parameters"></a>Параметры

*p*<br/>
окне Указатель на переменную, которая должна быть увеличена.

### <a name="return-value"></a>Возвращаемое значение

Если результат приращения равен 0, то функция **Increment** возвращает 0. Если результат инкремента равен нулю, то возвращаемое значение также будет ненулевым, но может не совпадать с результатом приращения.

### <a name="remarks"></a>Комментарии

**Интерлоккединкремент** предотвращает одновременное использование этой переменной более чем одним потоком.

## <a name="ccommultithreadmodelnocsthreadmodelnocs"></a><a name="threadmodelnocs"></a> Ккоммултисреадмоделнокс:: Среадмоделнокс

При использовании `CComMultiThreadModelNoCS` **`typedef`** имя `ThreadModelNoCS` просто ссылается на `CComMultiThreadModelNoCS` .

```
typedef CComMultiThreadModelNoCS ThreadModelNoCS;
```

### <a name="remarks"></a>Комментарии

[Ккоммултисреадмодел](../../atl/reference/ccommultithreadmodel-class.md) и [ккомсинглесреадмодел](../../atl/reference/ccomsinglethreadmodel-class.md) также содержат определения для `ThreadModelNoCS` . В следующей таблице показана связь между классом потоковой модели и классом, на который ссылается `ThreadModelNoCS` :

|Класс, определенный в|Ссылка на класс|
|----------------------|----------------------|
|`CComMultiThreadModelNoCS`|`CComMultiThreadModelNoCS`|
|`CComMultiThreadModel`|`CComMultiThreadModelNoCS`|
|`CComSingleThreadModel`|`CComSingleThreadModel`|

Обратите внимание, что определение `ThreadModelNoCS` в `CComMultiThreadModelNoCS` предоставляет симметрию с `CComMultiThreadModel` и `CComSingleThreadModel` . Например, предположим, что образец кода в `CComMultiThreadModel::AutoCriticalSection` объявлен следующим **`typedef`** образом:

[!code-cpp[NVC_ATL_COM#37](../../atl/codesnippet/cpp/ccommultithreadmodelnocs-class_1.h)]

Независимо от класса, указанного для `ThreadModel` (например `CComMultiThreadModelNoCS` ,), `_ThreadModel` разрешается соответствующим образом.

### <a name="example"></a>Пример

См. раздел [ккоммултисреадмодел:: аутокритикалсектион](../../atl/reference/ccommultithreadmodel-class.md#autocriticalsection).

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
