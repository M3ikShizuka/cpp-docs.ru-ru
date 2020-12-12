---
description: 'Дополнительные сведения о: Какцессор Class'
title: Класс CAccessor
ms.date: 11/04/2016
f1_keywords:
- ATL.CAccessor<T>
- ATL::CAccessor
- CAccessor
- ATL::CAccessor<T>
- ATL.CAccessor
helpviewer_keywords:
- CAccessor class
ms.assetid: b2ba959f-a686-46f3-8837-176248aef748
ms.openlocfilehash: 26b03bc3f464ce606194d6835953c39969bde5de
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97319174"
---
# <a name="caccessor-class"></a>Класс CAccessor

Представляет один из типов методов доступа.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
class CAccessor : public CAccessorBase, public T
```

### <a name="parameters"></a>Параметры

*T*<br/>
Класс записей пользователя.

## <a name="remarks"></a>Комментарии

Он используется, когда запись статически привязана к источнику данных. Запись содержит буфер. Этот класс поддерживает несколько методов доступа в наборе строк.

Используйте этот тип метода доступа, если известна структура и тип базы данных.

Если метод доступа содержит поля, указывающие на память (например, `BSTR` интерфейс или), которая должна быть освобождена, вызовите функцию-член [CAccessorRowset:: фрирекордмемори](./caccessorrowset-class.md#freerecordmemory) , прежде чем будет считано следующая запись.

## <a name="requirements"></a>Требования

**Заголовок:** atldbcli.h

## <a name="see-also"></a>См. также раздел

[Шаблоны объекта-получателя OLE DB](../../data/oledb/ole-db-consumer-templates-cpp.md)<br/>
[Справочник по шаблонам потребителей OLE DB](../../data/oledb/ole-db-consumer-templates-reference.md)
