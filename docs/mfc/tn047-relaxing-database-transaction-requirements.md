---
description: 'Дополнительные сведения о: TN047: требования к транзакциям базы данных отдыха'
title: TN047. Уменьшение требований к транзакциям баз данных
ms.date: 11/04/2016
f1_keywords:
- vc.data
helpviewer_keywords:
- TN047
ms.assetid: f93c51cf-a8c0-43d0-aa47-7bcb8333d693
ms.openlocfilehash: 6f356db75df93466bc392e555246a363e6b52187
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97215122"
---
# <a name="tn047-relaxing-database-transaction-requirements"></a>TN047. Уменьшение требований к транзакциям баз данных

Это техническое примечание, в котором обсуждались требования к транзакциям классов базы данных ODBC MFC, теперь устарело. До MFC 4,2 классы баз данных, требующие, чтобы курсоры сохранялись в наборах записей после выполнения операции **CommitTrans** или **ROLLBACK** . Если драйвер ODBC и СУБД не поддерживали такой уровень сохранения курсора, то классы базы данных не включили транзакции.

Начиная с MFC 4,2, классы базы данных имеют ослабленное ограничение на сохранение курсора. Транзакции будут включены, если они поддерживаются драйвером. Однако теперь необходимо проверить результат операции **CommitTrans** или **ROLLBACK** для открытых наборов записей. Дополнительные сведения см. в разделе функции элементов [CDatabase:: жеткурсоркоммитбехавиор](../mfc/reference/cdatabase-class.md#getcursorcommitbehavior) и [CDatabase:: жеткурсорроллбаккбехавиор](../mfc/reference/cdatabase-class.md#getcursorrollbackbehavior) .

## <a name="see-also"></a>См. также раздел

[Технические примечания по номеру](../mfc/technical-notes-by-number.md)<br/>
[Технические примечания по категориям](../mfc/technical-notes-by-category.md)
