---
description: 'Дополнительные сведения о: структура InterfaceListHelper'
title: InterfaceListHelper - структура
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::InterfaceListHelper
helpviewer_keywords:
- InterfaceListHelper structure
ms.assetid: 4297e419-c96b-45df-8a00-7568062125ba
ms.openlocfilehash: ca9e13e66acb6f27fba76a7653388305c57146dc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97249806"
---
# <a name="interfacelisthelper-structure"></a>InterfaceListHelper - структура

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
template <
    typename T0,
    typename T1 = Nil,
    typename T2 = Nil,
    typename T3 = Nil,
    typename T4 = Nil,
    typename T5 = Nil,
    typename T6 = Nil,
    typename T7 = Nil,
    typename T8 = Nil,
    typename T9 = Nil
>
struct InterfaceListHelper;

template <typename T0>
struct InterfaceListHelper<T0, Nil, Nil, Nil, Nil, Nil, Nil, Nil, Nil>;
```

### <a name="parameters"></a>Параметры

*T0*<br/>
Обязательный параметр шаблона 0.

*T1*<br/>
Параметр шаблона 1, который по умолчанию не задан.

*T2*<br/>
Параметр шаблона 2, который по умолчанию не задан. Третий параметр шаблона.

*T3*<br/>
Параметр шаблона 3, который по умолчанию не задан.

*T4*<br/>
Параметр шаблона 4, который по умолчанию не задан.

*T5*<br/>
Параметр шаблона 5, который по умолчанию не задан.

*T6*<br/>
Параметр шаблона 6, который по умолчанию не задан.

*T7*<br/>
Параметр шаблона 7, который по умолчанию не задан.

*T8*<br/>
Параметр шаблона 8, который по умолчанию не задан.

*T9*<br/>
Параметр шаблона 9, который по умолчанию не задан.

## <a name="remarks"></a>Комментарии

Создает `InterfaceList` тип, рекурсивно применяя заданные аргументы параметра шаблона.

Шаблон **InterfaceListHelper** использует параметр шаблона *T0* для определения первого элемента данных в `InterfaceList` структуре, а затем рекурсивно применяет шаблон **InterfaceListHelper** к любым оставшимся параметрам шаблона. **InterfaceListHelper** останавливается при отсутствии оставшихся параметров шаблона.

## <a name="members"></a>Элементы

### <a name="public-typedefs"></a>Общедоступные определения типов

|Имя|Описание|
|----------|-----------------|
|`TypeT`|Синоним для типа Интерфацелист.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`InterfaceListHelper`

## <a name="requirements"></a>Требования

**Заголовок:** Implements. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL::D состояния](microsoft-wrl-details-namespace.md)
