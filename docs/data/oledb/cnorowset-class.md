---
description: 'Дополнительные сведения о: Кноровсет Class'
title: Класс CNoRowset
ms.date: 11/04/2016
f1_keywords:
- ATL.CNoRowset
- ATL::CNoRowset<TAccessor>
- CNoRowset
- ATL.CNoRowset<TAccessor>
- ATL::CNoRowset
helpviewer_keywords:
- CNoRowset class
ms.assetid: 55c6c7a4-9e3a-4775-a2dd-c8b333012fa6
ms.openlocfilehash: 4cdb4631b63ec1f013183713900ffd9574d90fc3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97307565"
---
# <a name="cnorowset-class"></a>Класс CNoRowset

Может использоваться в качестве аргумента шаблона ( `TRowset` ) для [CCommand](../../data/oledb/ccommand-class.md) или [CTable](../../data/oledb/ctable-class.md).

## <a name="syntax"></a>Синтаксис

```cpp
template <class TAccessor = CAccessorBase>
class CNoRowset
```

### <a name="parameters"></a>Параметры

*такцессор*<br/>
Класс метода доступа. Значение по умолчанию — `CAccessorBase`.

## <a name="remarks"></a>Примечания

Используйте `CNoRowset` в качестве аргумента шаблона, если команда не возвращает набор строк.

`CNoRowset` реализует следующие методы-заглушки, каждый из которых соответствует другим методам класса метода доступа:

- `BindFinished` — Указывает, когда привязка завершена (Возвращает значение `S_OK` ).

- `Close` — Освобождает строки и текущий интерфейс IRowset.

- `GetIID` — Получает идентификатор интерфейса точки подключения.

- `GetInterface` — Извлекает интерфейс.

- `GetInterfacePtr` — Извлекает указатель инкапсулированного интерфейса.

- `SetAccessor` — Задает указатель на метод доступа.

- `SetupOptionalRowsetInterfaces` — Настраивает дополнительные интерфейсы для набора строк.

## <a name="requirements"></a>Требования

**Заголовок:** atldbcli.h

## <a name="see-also"></a>См. также раздел

[Шаблоны объекта-получателя OLE DB](../../data/oledb/ole-db-consumer-templates-cpp.md)<br/>
[Справочник по шаблонам потребителей OLE DB](../../data/oledb/ole-db-consumer-templates-reference.md)
