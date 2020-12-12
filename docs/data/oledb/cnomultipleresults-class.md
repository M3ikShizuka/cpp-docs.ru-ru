---
description: 'Дополнительные сведения о: CNoMultipleResults Class'
title: Класс CNoMultipleResults
ms.date: 11/04/2016
f1_keywords:
- CNoMultipleResults
- ATL.CNoMultipleResults
- ATL::CNoMultipleResults
helpviewer_keywords:
- CNoMultipleResults class
ms.assetid: 343e77c4-b319-476e-b592-901ab9b2f34e
ms.openlocfilehash: 1fd2ddfb19ed8fb4ba4fa3f957a77a2cc8312e1d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97170351"
---
# <a name="cnomultipleresults-class"></a>Класс CNoMultipleResults

Используется в качестве аргумента шаблона (*тмултипле*) [для создания](../../data/oledb/ccommand-class.md) оптимизированной команды, обрабатывающей один результирующий набор.

## <a name="syntax"></a>Синтаксис

```cpp
class CNoMultipleResults
```

## <a name="remarks"></a>Remarks

Если требуется, чтобы команда обрабатывала несколько результирующих наборов, используйте вместо него [CMultipleResults](../../data/oledb/cmultipleresults-class.md) .

## <a name="requirements"></a>Требования

**Заголовок:** atldbcli.h

## <a name="see-also"></a>См. также раздел

[Шаблоны объекта-получателя OLE DB](../../data/oledb/ole-db-consumer-templates-cpp.md)<br/>
[Справочник по шаблонам потребителей OLE DB](../../data/oledb/ole-db-consumer-templates-reference.md)
