---
description: 'Дополнительные сведения о: CDynamicStringAccessorA Class'
title: Класс CDynamicStringAccessorA
ms.date: 11/04/2016
f1_keywords:
- CDynamicStringAccessorA
helpviewer_keywords:
- CDynamicStringAccessorA class
ms.assetid: ed0d9821-a655-41f1-a902-43c3042ac49c
ms.openlocfilehash: 45a4d10c8a50c4009151fa90e51172405047a21a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97170728"
---
# <a name="cdynamicstringaccessora-class"></a>Класс CDynamicStringAccessorA

Позволяет получить доступ к источнику данных, если нет сведений о схеме базы данных (базовой структуре).

## <a name="syntax"></a>Синтаксис

```cpp
typedef CDynamicStringAccessorT<CHAR, DBTYPE_STR> CDynamicStringAccessorA;
```

## <a name="remarks"></a>Remarks

Они запрашивают, что поставщик извлекает все данные, доступ к которым осуществлялся из хранилища данных, в виде строковых данных, но `CDynamicStringAccessor` запрашивает строковые данные в формате ANSI.

`CDynamicStringAccessorA` наследует `GetString` и `SetString` из `CDynamicStringAccessor` . При использовании этих методов в `CDynamicStringAccessorA` объекте `BaseType` параметр имеет **тип char**.

## <a name="requirements"></a>Требования

**Заголовок**: Atldbcli. h

## <a name="see-also"></a>См. также раздел

[Шаблоны объекта-получателя OLE DB](../../data/oledb/ole-db-consumer-templates-cpp.md)<br/>
[Справочник по шаблонам потребителей OLE DB](../../data/oledb/ole-db-consumer-templates-reference.md)<br/>
[Класс Какцессор](../../data/oledb/caccessor-class.md)<br/>
[Класс CDynamicParameterAccessor](../../data/oledb/cdynamicparameteraccessor-class.md)<br/>
[Класс CManualAccessor](../../data/oledb/cmanualaccessor-class.md)<br/>
[Класс CDynamicAccessor](../../data/oledb/cdynamicaccessor-class.md)<br/>
[Класс CDynamicStringAccessor](../../data/oledb/cdynamicstringaccessor-class.md)<br/>
