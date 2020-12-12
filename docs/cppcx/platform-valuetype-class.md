---
description: 'Дополнительные сведения о классе Platform:: ValueType'
title: Platform::ValueType - класс
ms.date: 02/03/2017
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::ValueType::ToString
helpviewer_keywords:
- Platform::ValueType Class
ms.assetid: 79aa8754-b140-4974-a5b1-be046938a10a
ms.openlocfilehash: e6873b4b884586d06dae6e2fd1966041fd49bcc8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97307812"
---
# <a name="platformvaluetype-class"></a>Platform::ValueType - класс

Базовый класс для экземпляров типов значений.

## <a name="syntax"></a>Синтаксис

```cpp
public ref class ValueType : Object
```

## <a name="public-methods"></a>Открытые методы

| Имя | Описание |
|--|--|
| [ValueType:: ToString](#tostring) | Возвращает строковое представление объекта. Наследуется от [Platform:: Object](../cppcx/platform-object-class.md). |

### <a name="remarks"></a>Комментарии

Класс ValueType используется для создания типов значений. Класс ValueType является производным от класса Object, который содержит базовые элементы. Однако компилятор отсоединяет эти базовые элементы от типов значений, которые являются производными от класса ValueType. При упаковке типа значения компилятор снова присоединяет эти базовые элементы.

### <a name="requirements"></a>Требования

**Минимальный поддерживаемый клиент:** Windows 8

**Минимальный поддерживаемый сервер:** Windows Server 2012

**Пространство имен:** Platform

**Метаданные:** Platform. winmd

## <a name="valuetypetostring-method"></a><a name="tostring"></a> Метод ValueType:: ToString

Возвращает строковое представление объекта.

### <a name="syntax"></a>Синтаксис

```cpp
Platform::String ToString();
```

### <a name="return-value"></a>Возвращаемое значение

Строка Platform:: String, представляющая значение.

## <a name="see-also"></a>См. также раздел

[Пространство имен Platform](../cppcx/platform-namespace-c-cx.md)
