---
description: 'Дополнительные сведения о классе Platform:: MTAThreadAttribute'
title: Класс Platform::MTAThreadAttribute
ms.date: 12/30/2016
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::MTAThreadAttribute::Equals
- VCCORLIB/Platform::MTAThreadAttribute::GetHashCode
- VCCORLIB/Platform::MTAThreadAttribute::ToString
helpviewer_keywords:
- Platform::MTAThreadAttribute Class
ms.assetid: bfc546a7-4333-4407-85b4-4721565e1f44
ms.openlocfilehash: cc8586b37b4e5a1f6a6d0f33a27a21acca4aceb0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97308371"
---
# <a name="platformmtathreadattribute-class"></a>Класс Platform::MTAThreadAttribute

Указывает, что потоковая модель для приложения является многопотоковым подразделением (MTA).

## <a name="syntax"></a>Синтаксис

```
public ref class MTAThreadAttribute sealed : Attribute
```

### <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|Конструктор [MTAThreadAttribute 1](#ctor)|Инициализирует новый экземпляр класса.|

### <a name="public-methods"></a>Открытые методы

Атрибут MTAThreadAttribute наследует от [класса Platform:: Object](../cppcx/platform-object-class.md). Атрибут MTAThreadAttribute также перегружает или имеет следующие члены:

|Имя|Описание|
|----------|-----------------|
|[MTAThreadAttribute::Equals](#equals)|Определяет, равен ли указанный объект текущему объекту.|
|[MTAThreadAttribute::GetHashCode](#gethashcode)|Возвращает хэш-код данного экземпляра.|
|[MTAThreadAttribute::ToString](#tostring)|Возвращает строку, представляющую текущий объект.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`Platform`

### <a name="requirements"></a>Требования

**Метаданные:** Platform. winmd

**Пространство имен:** Platform

## <a name="mtathreadattribute-constructor"></a><a name="ctor"></a> Конструктор MTAThreadAttribute

Инициализирует новый экземпляр класса MTAThreadAttribute.

### <a name="syntax"></a>Синтаксис

```cpp
public:MTAThreadAttribute();
```

## <a name="mtathreadattributeequals"></a><a name="equals"></a> MTAThreadAttribute:: Equals

Определяет, равен ли указанный объект текущему объекту.

### <a name="syntax"></a>Синтаксис

```cpp
public:virtual override bool Equals( Object^ obj );
```

### <a name="parameters"></a>Параметры

*obj*<br/>
Объект для сравнения.

### <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если объекты равны; в противном случае — **`false`** .

## <a name="mtathreadattributegethashcode"></a><a name="gethashcode"></a> MTAThreadAttribute:: GetHashCode

Возвращает хэш-код данного экземпляра.

### <a name="syntax"></a>Синтаксис

```cpp
public:int GetHashCode();
```

### <a name="return-value"></a>Возвращаемое значение

Хэш-код данного экземпляра.

## <a name="mtathreadattributetostring"></a><a name="tostring"></a> MTAThreadAttribute:: ToString

Возвращает строку, представляющую текущий объект.

### <a name="syntax"></a>Синтаксис

```cpp
public:String^ ToString();
```

### <a name="return-value"></a>Возвращаемое значение

Строка, представляющая текущий объект.

## <a name="see-also"></a>См. также раздел

[Пространство имен платформы](platform-namespace-c-cx.md)
