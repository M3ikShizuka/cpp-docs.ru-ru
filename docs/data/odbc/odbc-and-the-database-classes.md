---
description: 'Дополнительные сведения: ODBC и классы базы данных'
title: ODBC и классы баз данных
ms.date: 11/04/2016
helpviewer_keywords:
- database classes [C++], ODBC
- ODBC API functions [C++]
- ODBC classes [C++], MFC database classes
- MFC [C++], ODBC and
ms.assetid: b166f82d-6f85-4556-aac8-fb851235d22c
ms.openlocfilehash: 146170ddd97dfc2797fd1f755459f370be638ded
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97326774"
---
# <a name="odbc-and-the-database-classes"></a>ODBC и классы баз данных

Классы базы данных MFC ODBC инкапсулируют вызовы функций API ODBC, которые обычно делают себя в функциях-членах классов [CDatabase](../../mfc/reference/cdatabase-class.md) и [CRecordset](../../mfc/reference/crecordset-class.md) . Например, сложные последовательности вызовов ODBC, привязка возвращаемых записей к местам хранения, обработка условий ошибок и другие операции управляются классами базы данных. В результате вы используете значительно более простой интерфейс класса для управления записями с помощью объекта набора записей.

> [!NOTE]
> Источники данных ODBC доступны через классы ODBC MFC, как описано в этом разделе, или через классы объектов доступа к данным MFC (DAO).

Несмотря на то что классы базы данных инкапсулируют функциональность ODBC, они не предоставляют однозначного сопоставления функций API ODBC. Классы баз данных обеспечивают более высокий уровень абстракции, смоделированный после обнаружения объектов доступа к данным в Microsoft Access и Microsoft Visual Basic. Дополнительные сведения см. в разделе [ODBC и MFC](../../data/odbc/odbc-and-mfc.md).

## <a name="see-also"></a>См. также раздел

[Основы ODBC](../../data/odbc/odbc-basics.md)
