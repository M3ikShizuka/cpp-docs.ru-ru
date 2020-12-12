---
description: 'Дополнительные сведения о: cancellation_token_registration классе'
title: Класс cancellation_token_registration
ms.date: 11/04/2016
f1_keywords:
- cancellation_token_registration
- PPLCANCELLATION_TOKEN/concurrency::cancellation_token_registration
- PPLCANCELLATION_TOKEN/concurrency::cancellation_token_registration::cancellation_token_registration
helpviewer_keywords:
- cancellation_token_registration class
ms.assetid: 823d63f4-7233-4d65-8976-6152ccf12d0e
ms.openlocfilehash: 1901e5132a9bad6849b1b00a6be63caf9afc9170
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97172145"
---
# <a name="cancellation_token_registration-class"></a>Класс cancellation_token_registration

Класс `cancellation_token_registration` представляет уведомление обратного вызова из `cancellation_token`. При использовании метода `register` на `cancellation_token` для получения уведомления о времени выполнения отмены объект `cancellation_token_registration` возвращается как дескриптор для обратного вызова, чтобы вызывающий код мог запросить, чтобы определенный обратный вызов больше не выполнялся с помощью метода `deregister`.

## <a name="syntax"></a>Синтаксис

```cpp
class cancellation_token_registration;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[cancellation_token_registration](#ctor)||
|[Деструктор ~ cancellation_token_registration](#dtor)||

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[operator! =](#operator_neq)||
|[Оператор =](#operator_eq)||
|[Оператор = =](#operator_eq_eq)||

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`cancellation_token_registration`

## <a name="requirements"></a>Требования

**Заголовок:** pplcancellation_token. h

**Пространство имен:** параллелизм

## <a name="cancellation_token_registration"></a><a name="dtor"></a> ~ cancellation_token_registration

```cpp
~cancellation_token_registration();
```

## <a name="cancellation_token_registration"></a><a name="ctor"></a> cancellation_token_registration

```cpp
cancellation_token_registration();

cancellation_token_registration(const cancellation_token_registration& _Src);

cancellation_token_registration(cancellation_token_registration&& _Src);
```

### <a name="parameters"></a>Параметры

*_Src*<br/>
`cancellation_token_registration`Копируемый или перемещаемый объект.

## <a name="operator"></a><a name="operator_neq"></a> operator! =

```cpp
bool operator!= (const cancellation_token_registration& _Rhs) const;
```

### <a name="parameters"></a>Параметры

*_Rhs*<br/>
Сравниваемый шаблон `cancellation_token_registration`.

### <a name="return-value"></a>Возвращаемое значение

## <a name="operator"></a><a name="operator_eq"></a> Оператор =

```cpp
cancellation_token_registration& operator= (const cancellation_token_registration& _Src);

cancellation_token_registration& operator= (cancellation_token_registration&& _Src);
```

### <a name="parameters"></a>Параметры

*_Src*<br/>
Объект `cancellation_token_registration` для назначения.

### <a name="return-value"></a>Возвращаемое значение

## <a name="operator"></a><a name="operator_eq_eq"></a> Оператор = =

```cpp
bool operator== (const cancellation_token_registration& _Rhs) const;
```

### <a name="parameters"></a>Параметры

*_Rhs*<br/>
Сравниваемый шаблон `cancellation_token_registration`.

### <a name="return-value"></a>Возвращаемое значение

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency](concurrency-namespace.md)
