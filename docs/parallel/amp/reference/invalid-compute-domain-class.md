---
description: 'Дополнительные сведения о: invalid_compute_domain классе'
title: invalid_compute_domain - класс
ms.date: 11/04/2016
f1_keywords:
- invalid_compute_domain
- AMPRT/invalid_compute_domain
- AMPRT/Concurrency::invalid_compute_domain::invalid_compute_domain
helpviewer_keywords:
- invalid_compute_domain class
ms.assetid: ac7a7166-8bdb-4db1-8caf-ea129ab5117e
ms.openlocfilehash: 7598180a12cacabcdb308c3924c84eb17ec90ed7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97329997"
---
# <a name="invalid_compute_domain-class"></a>invalid_compute_domain - класс

Исключение, возникающее, когда среда выполнения не может запустить ядро с помощью домена вычислений, указанного в [parallel_for_eachном](concurrency-namespace-functions-amp.md#parallel_for_each) месте вызова.

## <a name="syntax"></a>Синтаксис

```cpp
class invalid_compute_domain : public runtime_exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Конструктор invalid_compute_domain](#ctor)|Инициализирует новый экземпляр класса `invalid_compute_domain`.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`runtime_exception`

`invalid_compute_domain`

## <a name="requirements"></a>Требования

**Заголовок:** ампрт. h

**Пространство имен** : Concurrency

## <a name="invalid_compute_domain"></a><a name="ctor"></a> invalid_compute_domain

Инициализирует новый экземпляр класса.

### <a name="syntax"></a>Синтаксис

```cpp
explicit invalid_compute_domain(
    const char * _Message ) throw();

invalid_compute_domain() throw();
```

### <a name="parameters"></a>Параметры

*_Message*<br/>
Текстовое описание ошибки.

### <a name="return-value"></a>Возвращаемое значение

Экземпляр `invalid_compute_domain` класса

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency (C++ AMP)](concurrency-namespace-cpp-amp.md)
