---
description: 'Дополнительные сведения: Обмен полями записей (RFX)'
title: Обмен данными полями записей (RFX)
ms.date: 11/04/2016
helpviewer_keywords:
- RFX (ODBC) [C++]
- data [MFC], moving between sources and recordsets
- database classes [C++], RFX
- data [MFC]
- ODBC [C++], RFX
ms.assetid: f5ddfbf0-2901-48d7-9848-4fb84de3c7ee
ms.openlocfilehash: d181d779f74096dc035e9d492e50ef1823982b24
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97298894"
---
# <a name="record-field-exchange-rfx"></a>Обмен данными полями записей (RFX)

Классы базы данных MFC ODBC автоматизируют перемещение данных между источником данных и объектом [Recordset](../../data/odbc/recordset-odbc.md) . Если класс является производным от класса [CRecordset](../../mfc/reference/crecordset-class.md) и не использует групповые выборке строк, данные передаются механизмом обмена полями записей (RFX).

> [!NOTE]
> Если в производном классе реализована многострочная выборка строк `CRecordset` , то платформа использует механизм блочного обмена полями записей (массовым RFX) для перемещения данных. Дополнительные сведения см. [в разделе набор записей: групповая выборка записей (ODBC)](../../data/odbc/recordset-fetching-records-in-bulk-odbc.md).

RFX аналогичен обмену диалоговыми данными (DDX). Перемещение данных между источником данных и элементами данных поля набора записей требует нескольких вызовов функции [DoFieldExchange](../../mfc/reference/crecordset-class.md#dofieldexchange) набора записей и значительного взаимодействия между платформой и [ODBC](../../data/odbc/odbc-basics.md). Механизм RFX является типобезопасным и позволяет сохранить работу при вызове функций ODBC, таких как `::SQLBindCol` . Дополнительные сведения об DDX см [обмен данными окон и проверка](../../mfc/dialog-data-exchange-and-validation.md).

RFX в основном является прозрачным для вас. Если вы объявили классы наборов записей с помощью мастера приложений MFC или **добавите класс** (как описано в разделе [Добавление потребителя ODBC MFC](../../mfc/reference/adding-an-mfc-odbc-consumer.md)), RFX встроено в них автоматически. Класс набора записей должен быть производным от базового класса, `CRecordset` предоставляемого платформой. Мастер приложений MFC позволяет создать исходный класс набора записей. **Добавление класса** позволяет добавлять другие классы набора записей по мере необходимости. Дополнительные сведения и примеры см. [в разделе Добавление потребителя ODBC MFC](../../mfc/reference/adding-an-mfc-odbc-consumer.md).

В трех случаях необходимо вручную добавить небольшой объем кода RFX, если вы хотите:

- Используйте параметризованные запросы. Дополнительные сведения см. [в разделе набор записей: Параметризация набора записей (ODBC)](../../data/odbc/recordset-parameterizing-a-recordset-odbc.md).

- Выполнение соединений (с использованием одного набора записей для столбцов из двух или более таблиц). Дополнительные сведения см. [в разделе набор записей. Выполнение соединения (ODBC)](../../data/odbc/recordset-performing-a-join-odbc.md).

- Динамическое связывание столбцов данных. Это менее распространено, чем параметризация. Дополнительные сведения см. в разделе [набор записей: динамическая привязка столбцов данных (ODBC)](../../data/odbc/recordset-dynamically-binding-data-columns-odbc.md).

Если вам требуется более глубокое понимание RFX, см. раздел [запись обмена полями: принципы работы RFX](../../data/odbc/record-field-exchange-how-rfx-works.md).

В следующих разделах описаны сведения об использовании объектов Recordset.

- [Обмен полями записей: использование RFX](../../data/odbc/record-field-exchange-using-rfx.md)

- [Обмен полями записей: использование функций RFX](../../data/odbc/record-field-exchange-using-the-rfx-functions.md)

- [Обмен полями записей: принцип работы RFX](../../data/odbc/record-field-exchange-how-rfx-works.md)

## <a name="see-also"></a>См. также раздел

[Открытие подключения к базе данных (ODBC)](../../data/odbc/open-database-connectivity-odbc.md)<br/>
[Набор записей (ODBC)](../../data/odbc/recordset-odbc.md)<br/>
[Потребление MFC ODBC](../../mfc/reference/adding-an-mfc-odbc-consumer.md)<br/>
[Поддержка баз данных, мастер приложений MFC](../../mfc/reference/database-support-mfc-application-wizard.md)<br/>
[Класс CRecordset](../../mfc/reference/crecordset-class.md)
