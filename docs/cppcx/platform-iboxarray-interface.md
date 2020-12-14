---
description: 'Дополнительные сведения об интерфейсе Platform:: IBoxArray.'
title: Интерфейс Platform::IBoxArray
ms.date: 12/30/2016
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::IBoxArray
- VCCORLIB/Platform::IBoxArray::Value
helpviewer_keywords:
- Platform::IBoxArray
ms.assetid: 6cd82c9e-4230-4147-9edb-7a652875dbf1
ms.openlocfilehash: 8b87a00d709bec8af016de4532c7c4ec759d72fc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97195148"
---
# <a name="platformiboxarray-interface"></a>Интерфейс Platform::IBoxArray

`IBoxArray` является оболочкой для массивов типов значений, передаваемых через двоичный интерфейс приложений (ABI) или хранящихся в коллекциях элементов `Platform::Object^` , таких как коллекции в элементах управления XAML.

## <a name="syntax"></a>Синтаксис

```cpp
template <typename T>
interface class IBoxArray
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Тип упакованного значение в каждом элементе массива.

### <a name="remarks"></a>Комментарии

`IBoxArray` — имя C++/CX для `Windows::Foundation::IReferenceArray` .

### <a name="members"></a>Элементы

Интерфейс `IBoxArray` наследует от интерфейса `IValueType` . Интерфейс`IBoxArray` также содержит следующие члены:

|Метод|Описание|
|------------|-----------------|
|[Значение](#value)|Возвращает распакованный массив, который ранее хранился в этом экземпляре `IBoxArray` .|

## <a name="iboxarrayvalue-property"></a><a name="value"></a> Свойство IBoxArray:: value

Возвращает значение, которое было изначально сохранено в этом объекте.

### <a name="syntax"></a>Синтаксис

```cpp
property T Value {T get();}
```

### <a name="parameters"></a>Параметры

*T*<br/>
Введите запакованное значение.

### <a name="property-valuereturn-value"></a>Значение свойства/возвращаемое значение

Возвращает значение, которое было изначально сохранено в этом объекте.

### <a name="remarks"></a>Комментарии

Пример см. в разделе [Упаковка](../cppcx/boxing-c-cx.md).

## <a name="see-also"></a>См. также раздел

[Классы Array и WriteOnlyArray](../cppcx/array-and-writeonlyarray-c-cx.md)
