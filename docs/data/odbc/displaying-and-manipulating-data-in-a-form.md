---
description: 'Дополнительные сведения: отображение и обработка данных в форме'
title: Отображение и обработка данных в форме
ms.date: 11/04/2016
helpviewer_keywords:
- forms [C++], displaying data
- displaying data [C++], forms
- ODBC [C++], forms
- record views [C++], displaying data
- data [MFC]
- data [MFC], displaying in a form
ms.assetid: c56185c4-12cb-40b1-b499-02b29ea83e3a
ms.openlocfilehash: 151e4036830f4923fbed2e609535edf3beacee5f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97252328"
---
# <a name="displaying-and-manipulating-data-in-a-form"></a>Отображение и обработка данных в форме

Многие приложения для доступа к данным выбирают данные и отображают их в полях формы. Класс базы данных [CRecordView](../../mfc/reference/crecordview-class.md) предоставляет объект [CFormView](../../mfc/reference/cformview-class.md) , непосредственно подключенный к объекту Recordset. Представление записей использует [Обмен данными диалогового окна (DDX)](../../mfc/dialog-data-exchange-and-validation.md) для перемещения значений полей текущей записи из набора записей в элементы управления в форме и для перемещения обновленной информации обратно в набор записей. Набор записей, в свою очередь, использует обмен полями записей (RFX) для перемещения данных между элементами данных поля и соответствующими столбцами в таблице в источнике данных.

Можно использовать мастер приложений MFC или **Добавить класс** (как описано в разделе [Добавление потребителя ODBC MFC](../../mfc/reference/adding-an-mfc-odbc-consumer.md)), чтобы создать класс представления и связанный с ним класс набора записей в сочетании.

Представление записей и его набор записей уничтожаются при закрытии документа. Дополнительные сведения о представлениях записей см. в разделе [представления записей](../../data/record-views-mfc-data-access.md). Дополнительные сведения о RFX см. в статье [Обмен полями записей (RFX)](../../data/odbc/record-field-exchange-rfx.md).

## <a name="see-also"></a>См. также раздел

[ODBC и MFC](../../data/odbc/odbc-and-mfc.md)
