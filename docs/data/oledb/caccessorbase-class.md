---
description: 'Дополнительные сведения о: CAccessorBase Class'
title: Класс CAccessorBase
ms.date: 11/04/2016
f1_keywords:
- CAccessorBase
- CAccessorBase.Close
- CAccessorBase::Close
- GetHAccessor
- CAccessorBase::GetHAccessor
- CAccessorBase.GetHAccessor
- CAccessorBase::GetNumAccessors
- GetNumAccessors
- CAccessorBase.GetNumAccessors
- IsAutoAccessor
- CAccessorBase.IsAutoAccessor
- CAccessorBase::IsAutoAccessor
- CAccessorBase::ReleaseAccessors
- CAccessorBase.ReleaseAccessors
- ReleaseAccessors
helpviewer_keywords:
- CAccessorBase class
- Close method
- GetHAccessor method
- GetNumAccessors method
- IsAutoAccessor method
- ReleaseAccessors method
ms.assetid: 389b65be-11ca-4ae0-9290-60c621c4982b
ms.openlocfilehash: 43d3f507f8ee003605cf2b3f964b06a3c1088233
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97221180"
---
# <a name="caccessorbase-class"></a>Класс CAccessorBase

Все методы доступа в шаблонах OLE DB являются производными от этого класса. `CAccessorBase` позволяет одному набору строк управлять множеством методов доступа. Он также предоставляет привязку для параметров и выходных столбцов.

## <a name="syntax"></a>Синтаксис

```cpp
// Replace with syntax
```

## <a name="members"></a>Члены

### <a name="methods"></a>Методы

| Имя | Описание |
|--|--|
| [Закрыть](#close) | Закрывает методы доступа. |
| [жесакцессор](#geth) | Извлекает маркер метода доступа. |
| [жетнумакцессорс](#getnum) | Возвращает количество методов доступа, созданных классом. |
| [исаутоакцессор](#isauto) | Проверяет, является ли указанный метод доступа автоматическим. |
| [релеасеакцессорс](#release) | Освобождает методы доступа. |

## <a name="requirements"></a>Требования

**Заголовок:** atldbcli.h

## <a name="caccessorbaseclose"></a><a name="close"></a> CAccessorBase:: Close

Закрывает методы доступа.

### <a name="syntax"></a>Синтаксис

```cpp
void Close();
```

### <a name="remarks"></a>Remarks

Сначала необходимо вызвать [релеасеакцессорс](#release) .

## <a name="caccessorbasegethaccessor"></a><a name="geth"></a> CAccessorBase:: Жесакцессор

Получает маркер метода доступа для указанного метода доступа.

### <a name="syntax"></a>Синтаксис

```cpp
HACCESSOR GetHAccessor(ULONG nAccessor) const;
```

#### <a name="parameters"></a>Параметры

*накцессор*<br/>
окне Число с нулевым смещением для метода доступа.

### <a name="return-value"></a>Возвращаемое значение

Обработчик метода доступа.

## <a name="caccessorbasegetnumaccessors"></a><a name="getnum"></a> CAccessorBase:: Жетнумакцессорс

Возвращает количество методов доступа, созданных классом.

### <a name="syntax"></a>Синтаксис

```cpp
ULONG GetNumAccessors() const;
```

### <a name="return-value"></a>Возвращаемое значение

Количество методов доступа, созданных классом.

## <a name="caccessorbaseisautoaccessor"></a><a name="isauto"></a> CAccessorBase:: Исаутоакцессор

Возвращает значение true, если данные автоматически извлекаются для метода доступа во время операции перемещения.

### <a name="syntax"></a>Синтаксис

```cpp
bool IsAutoAccessor(ULONG nAccessor) const;
```

#### <a name="parameters"></a>Параметры

*накцессор*<br/>
окне Число с нулевым смещением для метода доступа.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение, **`true`** Если метод доступа является автоматическим. В противном случае возвращается значение **`false`** .

## <a name="caccessorbasereleaseaccessors"></a><a name="release"></a> CAccessorBase:: Релеасеакцессорс

Освобождает методы доступа, созданные классом.

### <a name="syntax"></a>Синтаксис

```cpp
HRESULT ReleaseAccessors(IUnknown* pUnk);
```

#### <a name="parameters"></a>Параметры

*pUnk*<br/>
окне Указатель на `IUnknown` интерфейс для COM-объекта, для которого были созданы методы доступа.

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

### <a name="remarks"></a>Комментарии

Вызывается из [CAccessorRowset:: Close](./caccessorrowset-class.md#close).

## <a name="see-also"></a>См. также раздел

[Шаблоны объекта-получателя OLE DB](../../data/oledb/ole-db-consumer-templates-cpp.md)<br/>
[Справочник по шаблонам потребителей OLE DB](../../data/oledb/ole-db-consumer-templates-reference.md)<br/>
[Класс CAccessorBase](../../data/oledb/caccessorbase-class.md)
