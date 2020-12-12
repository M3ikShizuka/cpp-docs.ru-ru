---
description: 'Дополнительные сведения о: accelerator_view_removed классе'
title: Класс accelerator_view_removed
ms.date: 03/27/2019
f1_keywords:
- accelerator_view_removed
- AMPRT/accelerator_view_removed
- AMPRT/Concurrency::accelerator_view_removed::accelerator_view_removed
- AMPRT/Concurrency::accelerator_view_removed::get_view_removed_reason
helpviewer_keywords:
- AMPRT/Concurrency::accelerator_view_removed::accelerator_view_removed Class
ms.assetid: 262446de-311c-454e-a5ed-e2aaced0d88a
ms.openlocfilehash: 86a5b89d3b8065bccd8eec8b10bade9ed26d6a05
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97254499"
---
# <a name="accelerator_view_removed-class"></a>Класс accelerator_view_removed

Исключение, возникающее при сбое базового вызова DirectX из-за обнаружения времени ожидания Windows и механизма восстановления.

## <a name="syntax"></a>Синтаксис

```cpp
class accelerator_view_removed : public runtime_exception;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Конструктор accelerator_view_removed](#ctor)|Инициализирует новый экземпляр класса `accelerator_view_removed`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[get_view_removed_reason](#get_view_removed_reason)|Возвращает код ошибки HRESULT, указывающий на причину `accelerator_view` удаления объекта.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`exception`

`runtime_exception`

`out_of_memory`

## <a name="requirements"></a>Требования

**Заголовок:** ампрт. h

**Пространство имен** : Concurrency

## <a name="accelerator_view_removed"></a><a name="ctor"></a> accelerator_view_removed

Инициализирует новый экземпляр класса [accelerator_view_removed](accelerator-view-removed-class.md) .

### <a name="syntax"></a>Синтаксис

```cpp
explicit accelerator_view_removed(
    const char * message,
    HRESULT view_removed_reason ) throw();

explicit accelerator_view_removed(
    HRESULT view_removed_reason ) throw();
```

### <a name="parameters"></a>Параметры

*message*<br/>
Текстовое описание ошибки.

*view_removed_reason*<br/>
Код ошибки HRESULT, указывающий причину удаления `accelerator_view` объекта.

### <a name="return-value"></a>Возвращаемое значение

Новый экземпляр класса `accelerator_view_removed`.

## <a name="get_view_removed_reason"></a><a name="get_view_removed_reason"></a> get_view_removed_reason

Возвращает код ошибки HRESULT, указывающий на причину `accelerator_view` удаления объекта.

### <a name="syntax"></a>Синтаксис

```cpp
HRESULT get_view_removed_reason() const throw();
```

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency (C++ AMP)](concurrency-namespace-cpp-amp.md)
