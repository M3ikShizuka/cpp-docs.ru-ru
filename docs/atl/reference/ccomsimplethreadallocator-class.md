---
description: 'Дополнительные сведения о: Ккомсимплесреадаллокатор Class'
title: Класс Ккомсимплесреадаллокатор
ms.date: 11/04/2016
f1_keywords:
- CComSimpleThreadAllocator
- ATLBASE/ATL::CComSimpleThreadAllocator
- ATLBASE/ATL::CComSimpleThreadAllocator::GetThread
helpviewer_keywords:
- threading [ATL], selecting threads
- ATL threads
- CComSimpleThreadAllocator class
- ATL threads, allocating
ms.assetid: 66b2166a-8c50-49fd-b8e4-7f293470327d
ms.openlocfilehash: 5925707ecd459475d9e9002af76fb76dd9cf9d38
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142191"
---
# <a name="ccomsimplethreadallocator-class"></a>Класс Ккомсимплесреадаллокатор

Этот класс управляет выбором потоков для класса `CComAutoThreadModule` .

## <a name="syntax"></a>Синтаксис

```
class CComSimpleThreadAllocator
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккомсимплесреадаллокатор:: Thread](#getthread)|Выбирает поток.|

## <a name="remarks"></a>Комментарии

`CComSimpleThreadAllocator` управляет выбором потоков для [ккомаутосреадмодуле](../../atl/reference/ccomautothreadmodule-class.md). `CComSimpleThreadAllocator::GetThread` просто циклически перебирает каждый поток и возвращает следующий объект в последовательности.

## <a name="requirements"></a>Требования

**Заголовок:** atlbase. h

## <a name="ccomsimplethreadallocatorgetthread"></a><a name="getthread"></a> Ккомсимплесреадаллокатор:: Thread

Выбирает поток, указывая следующий поток в последовательности.

```
int GetThread(CComApartment* /* pApt */, int nThreads);
```

### <a name="parameters"></a>Параметры

*папт*<br/>
Не используется в реализации ATL по умолчанию.

*нсреадс*<br/>
Максимальное число потоков в модуле EXE.

### <a name="return-value"></a>Возвращаемое значение

Целое число от 0 до (*нсреадс* -1). Определяет один из потоков в модуле EXE.

### <a name="remarks"></a>Комментарии

Можно переопределить `GetThread` , чтобы предоставить другой метод выбора или использовать параметр *папт* .

`GetThread` метод вызывается методом [ккомаутосреадмодуле:: CreateInstance](../../atl/reference/ccomautothreadmodule-class.md#createinstance).

## <a name="see-also"></a>См. также раздел

[Класс Ккомапартмент](../../atl/reference/ccomapartment-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
