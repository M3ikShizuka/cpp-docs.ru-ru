---
description: 'Дополнительные сведения: Преобразование данных, не поддерживаемых поставщиком'
title: Преобразование данных, не поддерживаемых поставщиком
ms.date: 10/29/2018
helpviewer_keywords:
- OLE DB provider templates, unsupported data types
ms.assetid: f495e50f-530a-4fab-ab54-e0c359785845
ms.openlocfilehash: 9fb449247ff40118e89dbebee5f43a1208a1f181
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323370"
---
# <a name="converting-data-not-supported-by-the-provider"></a>Преобразование данных, не поддерживаемых поставщиком

Когда потребитель запрашивает тип данных, который не поддерживается поставщиком, код шаблона поставщика OLE DB для `IRowsetImpl::GetData` вызовов Msdadc.dll для преобразования типа данных.

При реализации интерфейса `IRowsetChange` , который требует преобразования данных, можно вызвать Msdaenum.dll, чтобы выполнить преобразование. Используйте `GetData` , определенный в ATLDB. h, как пример.

## <a name="see-also"></a>См. также раздел

[Работа с шаблонами поставщика OLE DB](../../data/oledb/working-with-ole-db-provider-templates.md)
