---
description: 'Дополнительные сведения о: RoInitializeWrapper Class'
title: Класс RoInitializeWrapper
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::RoInitializeWrapper
- corewrappers/Microsoft::WRL::Wrappers::RoInitializeWrapper::HRESULT
- corewrappers/Microsoft::WRL::Wrappers::RoInitializeWrapper::RoInitializeWrapper
- corewrappers/Microsoft::WRL::Wrappers::RoInitializeWrapper::~RoInitializeWrapper
helpviewer_keywords:
- Microsoft::WRL::Wrappers::RoInitializeWrapper class
- Microsoft::WRL::Wrappers::RoInitializeWrapper::operator HRESULT operator
- Microsoft::WRL::Wrappers::RoInitializeWrapper::RoInitializeWrapper, constructor
- Microsoft::WRL::Wrappers::RoInitializeWrapper::~RoInitializeWrapper, destructor
ms.assetid: 4055fbe0-63a7-4c06-b5a0-414fda5640e5
ms.openlocfilehash: b7f2c49bd461f08ad732680f1a02968ee7717116
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97319304"
---
# <a name="roinitializewrapper-class"></a>Класс RoInitializeWrapper

Инициализирует среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```cpp
class RoInitializeWrapper;
```

## <a name="remarks"></a>Remarks

`RoInitializeWrapper` — Это удобство, которое инициализирует среда выполнения Windows и возвращает значение HRESULT, указывающее, была ли операция успешной. Поскольку деструктор класса вызывает `::Windows::Foundation::Uninitialize` , экземпляры `RoInitializeWrapper` должны быть объявлены на глобальном уровне или области верхнего уровня.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

name                                                                    | Описание
----------------------------------------------------------------------- | -----------------------------------------------------------------
[RoInitializeWrapper:: RoInitializeWrapper](#roinitializewrapper)        | Инициализирует новый экземпляр класса `RoInitializeWrapper`.
[RoInitializeWrapper:: ~ RoInitializeWrapper](#tilde-roinitializewrapper) | Уничтожает текущий экземпляр `RoInitializeWrapper` класса.

### <a name="public-operators"></a>Открытые операторы

Имя                                       | Описание
------------------------------------------ | ------------------------------------------------------------------------
[RoInitializeWrapper:: HRESULT ()](#hresult) | Извлекает значение HRESULT, созданное `RoInitializeWrapper` конструктором.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`RoInitializeWrapper`

## <a name="requirements"></a>Требования

**Заголовок:** кореврапперс. h

**Пространство имен:** Программы Microsoft:: WRL:: оболочки

## <a name="roinitializewrapperhresult"></a><a name="hresult"></a> RoInitializeWrapper:: HRESULT ()

Извлекает значение HRESULT, созданное последним `RoInitializeWrapper` конструктором.

```cpp
operator HRESULT()
```

## <a name="roinitializewrapperroinitializewrapper"></a><a name="roinitializewrapper"></a> RoInitializeWrapper:: RoInitializeWrapper

Инициализирует новый экземпляр класса `RoInitializeWrapper`.

```cpp
RoInitializeWrapper(RO_INIT_TYPE flags)
```

### <a name="parameters"></a>Параметры

*flags*<br/>
Одно из перечислений RO_INIT_TYPE, которое указывает поддержку, предоставляемую среда выполнения Windows.

### <a name="remarks"></a>Комментарии

`RoInitializeWrapper`Класс вызывает `Windows::Foundation::Initialize(flags)` .

## <a name="roinitializewrapperroinitializewrapper"></a><a name="tilde-roinitializewrapper"></a> RoInitializeWrapper:: ~ RoInitializeWrapper

Отменяет инициализацию среда выполнения Windows.

```cpp
~RoInitializeWrapper()
```

### <a name="remarks"></a>Комментарии

`RoInitializeWrapper`Класс вызывает `Windows::Foundation::Uninitialize()` .
