---
description: 'Дополнительные сведения: класс значений Platform:: resize'
title: Класс значения Platform::SizeT
ms.date: 12/30/2016
ms.topic: reference
f1_keywords:
- VCCORLIB/PlatformSizeT::SizeT constructor
helpviewer_keywords:
- Platform::SizeT Struct
ms.assetid: 0803612c-8ba1-430c-9b7b-1bebae88608d
ms.openlocfilehash: ebcca27a94d23082374daafaa9fd7db180955a30
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97308020"
---
# <a name="platformsizet-value-class"></a>Класс значения Platform::SizeT

Представляет размер объекта. SizeT — беззнаковый тип данных.

## <a name="syntax"></a>Синтаксис

```cpp
public ref class SizeT sealed : ValueType
```

### <a name="members"></a>Члены

|Член|Описание|
|------------|-----------------|
|[Конструктор SizeT::SizeT](#ctor)|Инициализирует новый экземпляр класса, используя указанное значение.|

### <a name="requirements"></a>Требования

**Минимальный поддерживаемый клиент:** Windows 8

**Минимальный поддерживаемый сервер:** Windows Server 2012

**Пространство имен:** Platform

**Метаданные:** Platform. winmd

## <a name="sizetsizet-constructor"></a><a name="ctor"></a> Конструктор размера:: size

Инициализирует новый экземпляр класса SizeT указанным значением.

### <a name="syntax"></a>Синтаксис

```cpp
SizeT( uint32 value1 );   SizeT( void* value2 );
```

### <a name="parameters"></a>Параметры

*Значение1*<br/>
32-битовое значение без знака.

*value2*<br/>
Указатель на 32-разрядное значение без знака.

## <a name="see-also"></a>См. также раздел

[Пространство имен Platform](../cppcx/platform-namespace-c-cx.md)
