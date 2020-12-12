---
description: 'Дополнительные сведения о: CDynamicStringAccessorW Class'
title: Класс CDynamicStringAccessorW
ms.date: 11/04/2016
f1_keywords:
- CDynamicStringAccessorW
helpviewer_keywords:
- CDynamicStringAccessorW class
ms.assetid: 9b7fd5cc-3a9b-4b57-b907-f1e35de2c98f
ms.openlocfilehash: 360a9592cdce3a1046eecb360a8691b1d8480caf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97170676"
---
# <a name="cdynamicstringaccessorw-class"></a>Класс CDynamicStringAccessorW

Позволяет получить доступ к источнику данных, если нет сведений о схеме базы данных (базовой структуре).

## <a name="syntax"></a>Синтаксис

```cpp
typedef CDynamicStringAccessorT<WCHAR, DBTYPE_WSTR> CDynamicStringAccessorW;
```

## <a name="remarks"></a>Remarks

Они запрашивают, что поставщик извлекает все данные, доступ к которым осуществлялся из хранилища данных, в виде строковых данных, но `CDynamicStringAccessor` запрашивает строковые данные в Юникоде.

`CDynamicStringAccessorW` наследует `GetString` и `SetString` из `CDynamicStringAccessor` . При использовании этих методов в `CDynamicStringAccessorW` объекте `BaseType` параметр имеет значение **WCHAR**.

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
