---
description: 'Дополнительные сведения о: Ккомаутокритикалсектион Class'
title: Класс Ккомаутокритикалсектион
ms.date: 11/04/2016
f1_keywords:
- CComAutoCriticalSection
- ATLCORE/ATL::CComAutoCriticalSection
- ATLCORE/ATL::CComAutoCriticalSection::CComAutoCriticalSection
helpviewer_keywords:
- CComAutoCriticalSection class
ms.assetid: 491a9d90-3398-4f90-88f5-fd2172a46b30
ms.openlocfilehash: 2441c714b95a3bbefed4a699055d14c6915cffda
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97146969"
---
# <a name="ccomautocriticalsection-class"></a>Класс Ккомаутокритикалсектион

`CComAutoCriticalSection` предоставляет методы для получения и освобождения владельца объекта критической секции.

## <a name="syntax"></a>Синтаксис

```
class CComAutoCriticalSection : public CComCriticalSection
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккомаутокритикалсектион:: Ккомаутокритикалсектион](#ccomautocriticalsection)|Конструктор.|
|[Ккомаутокритикалсектион:: ~ Ккомаутокритикалсектион](#dtor)|Деструктор|

## <a name="remarks"></a>Комментарии

`CComAutoCriticalSection` аналогичен классу [ккомкритикалсектион](../../atl/reference/ccomcriticalsection-class.md), за исключением `CComAutoCriticalSection` автоматической инициализации объекта критической секции в конструкторе.

Обычно используется `CComAutoCriticalSection` **`typedef`** имя [аутокритикалсектион](ccommultithreadmodel-class.md#autocriticalsection). Это имя указывает, `CComAutoCriticalSection` когда используется [ккоммултисреадмодел](../../atl/reference/ccommultithreadmodel-class.md) .

`Init`Методы и `Term` из [ккомкритикалсектион](../../atl/reference/ccomcriticalsection-class.md) недоступны при использовании этого класса.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[ккомкритикалсектион](../../atl/reference/ccomcriticalsection-class.md)

`CComAutoCriticalSection`

## <a name="requirements"></a>Требования

**Заголовок:** атлкоре. h

## <a name="ccomautocriticalsectionccomautocriticalsection"></a><a name="ccomautocriticalsection"></a> Ккомаутокритикалсектион:: Ккомаутокритикалсектион

Конструктор.

```
CComAutoCriticalSection();
```

### <a name="remarks"></a>Комментарии

Вызывает функцию Win32 [инитиализекритикалсектион](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsection), которая инициализирует объект критической секции.

## <a name="ccomautocriticalsectionccomautocriticalsection"></a><a name="dtor"></a> Ккомаутокритикалсектион:: ~ Ккомаутокритикалсектион

Деструктор

```
~CComAutoCriticalSection() throw();
```

### <a name="remarks"></a>Комментарии

Деструктор вызывает [делетекритикалсектион](/windows/win32/api/synchapi/nf-synchapi-deletecriticalsection), который освобождает все системные ресурсы, используемые объектом критического раздела.

## <a name="see-also"></a>См. также раздел

[Класс Ккомфакекритикалсектион](../../atl/reference/ccomfakecriticalsection-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)<br/>
[Класс Ккомкритикалсектион](../../atl/reference/ccomcriticalsection-class.md)
