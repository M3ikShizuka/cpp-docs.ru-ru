---
description: 'Дополнительные сведения о: CColumnAccessor Class'
title: Класс CColumnAccessor
ms.date: 11/04/2016
f1_keywords:
- CColumnAccessor
- ATL::CColumnAccessor
- ATL.CColumnAccessor
helpviewer_keywords:
- CColumnAccessor class
ms.assetid: 6ce1e67f-6a20-490d-9326-c168b43eee7e
ms.openlocfilehash: 7551f39d34bb4f13b4ffae358db05aede2adb9e5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335526"
---
# <a name="ccolumnaccessor-class"></a>Класс CColumnAccessor

Создает код для внедренного потребителя.

## <a name="syntax"></a>Синтаксис

```cpp
class CColumnAccessor : public CAccessorBase
```

## <a name="remarks"></a>Remarks

В введенном коде каждый столбец привязан как отдельный метод доступа. Следует иметь в виду, что этот класс используется во внедренном коде (например, при отладке), но обычно его не нужно использовать напрямую или непосредственно с его методами.

`CColumnAccessor` реализует следующие методы-заглушки, каждый из которых соответствует функциональным возможностям другим методам класса методов доступа:

- `CColumnAccessor` Конструктор; создает и инициализирует `CColumnAccessor` объект.

- `CreateAccessor` Выделяет память для структур привязки столбцов и инициализирует элементы данных столбца.

- `BindColumns` Привязывает столбцы к методы доступа.

- `SetParameterBuffer` Выделяет буферы для параметров.

- `AddParameter` Добавляет запись параметра в структуры записи параметра.

- `HasOutputColumns` Определяет, содержит ли метод доступа выходные столбцы.

- `HasParameters` Определяет, имеет ли метод доступа параметры.

- `BindParameters` Привязывает созданные параметры к столбцам.

## <a name="requirements"></a>Требования

**Заголовок:** atldbcli.h

## <a name="see-also"></a>См. также раздел

[Шаблоны объекта-получателя OLE DB](../../data/oledb/ole-db-consumer-templates-cpp.md)<br/>
[Справочник по шаблонам потребителей OLE DB](../../data/oledb/ole-db-consumer-templates-reference.md)
