---
description: 'Дополнительные сведения о: Кноакцессор Class'
title: Класс CNoAccessor
ms.date: 11/04/2016
f1_keywords:
- ATL::CNoAccessor
- CNoAccessor
- ATL.CNoAccessor
helpviewer_keywords:
- CNoAccessor class
ms.assetid: eb669ae5-0a56-49a3-9646-c4ae6239da31
ms.openlocfilehash: 624c72c841280ec56bacf0edd29efeb4b1005988
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97170390"
---
# <a name="cnoaccessor-class"></a>Класс CNoAccessor

Может использоваться в качестве аргумента шаблона ( `TAccessor` ) для классов шаблонов, таких как `CCommand` и `CTable` , для которых требуется аргумент класса метода доступа.

## <a name="syntax"></a>Синтаксис

```cpp
class CNoAccessor
```

## <a name="remarks"></a>Remarks

Используйте `CNoAccessor` в качестве аргумента шаблона, если не требуется, чтобы класс поддерживал параметры или выходные столбцы.

`CNoAccessor` реализует следующие методы-заглушки, каждый из которых соответствует другим методам класса метода доступа:

- `BindColumns` — Привязывает столбцы к методы доступа.

- `BindParameters` — Привязывает созданные параметры к столбцам.

- `Bind` — Создает привязки.

- `Close` — Закрывает метод доступа.

- `ReleaseAccessors` — Освобождает методы доступа, созданные классом.

- `FreeRecordMemory` — Освобождает все столбцы в текущей записи, которые необходимо освободить.

- `GetColumnInfo` — Получает сведения о столбцах из открытого набора строк.

- `GetNumAccessors` — Получает количество методов доступа, созданных классом.

- `IsAutoAccessor` — Возвращает значение true, если данные автоматически извлекаются для метода доступа во время операции перемещения.

- `GetHAccessor` — Получает маркер метода доступа для указанного метода доступа.

- `GetBuffer` — Получает указатель на буфер закладки.

- `NoBindOnNullRowset` — Предотвращает привязку данных к пустым наборам строк.

## <a name="requirements"></a>Требования

**Заголовок:** atldbcli.h

## <a name="see-also"></a>См. также раздел

[Шаблоны объекта-получателя OLE DB](../../data/oledb/ole-db-consumer-templates-cpp.md)<br/>
[Справочник по шаблонам потребителей OLE DB](../../data/oledb/ole-db-consumer-templates-reference.md)
