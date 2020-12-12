---
description: 'Дополнительные сведения: улучшение простого поставщика Read-Only'
title: Усовершенствование простого поставщика только для чтения
ms.date: 10/26/2018
helpviewer_keywords:
- read-only poviders [C++]
- IRowsetLocate class
- IRowsetLocate class, adding to OLE DB template providers
- simple read-only poviders [C++]
ms.assetid: cba0e09f-44c1-41c1-9456-332aa13dc158
ms.openlocfilehash: 00a0ea4fb9b759447026353ba0d78c7c856b15ae
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97317640"
---
# <a name="enhancing-the-simple-read-only-provider"></a>Усовершенствование простого поставщика только для чтения

В этом разделе показано, как расширить [простой поставщик только для чтения](../../data/oledb/implementing-the-simple-read-only-provider.md) , созданный в предыдущем разделе. `IRowsetLocateImpl` Создает реализацию для `IRowsetLocate` интерфейса и добавляет поддержку закладок.

При наличии рабочего поставщика может потребоваться усовершенствовать его, чтобы обновить поставщик, обработайте транзакции или повысить производительность алгоритма выборки строк. Большинство улучшений поставщика подразумевает Добавление интерфейса в существующий COM-объект.

В примере в следующих разделах механизм выборки строк расширяется путем добавления `IRowsetLocate` интерфейса в `CAgentRowset` . В этом разделе показано, как:

- [Сделать ркустомровсет производным от IRowsetLocate](../../data/oledb/modifying-the-inheritance-of-rmyproviderrowset.md).

- [Динамически определяются столбцы, возвращаемые потребителю](../../data/oledb/dynamically-determining-columns-returned-to-the-consumer.md).

## <a name="see-also"></a>См. также раздел

[Создание простого поставщика Read-Only](../../data/oledb/creating-a-simple-read-only-provider.md)<br/>
