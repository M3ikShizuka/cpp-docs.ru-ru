---
description: 'Дополнительные сведения: использование представлений записей OLE DB'
title: Использование представлений записей OLE DB
ms.date: 10/24/2018
helpviewer_keywords:
- OLE DB record views
- COleDBRecordView class, overview
- rowsets, record views
- record views, record view objects
- OLE DB, record views
- MFC, record views
ms.assetid: 1cd3e595-ce08-43d8-a0a9-d03b5d3e24ce
ms.openlocfilehash: 8230ba118038852f81159d21a51165b7448a26aa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332455"
---
# <a name="using-ole-db-record-views"></a>Использование представлений записей OLE DB

Если требуется отобразить данные набора строк OLE DB в приложении MFC, используйте класс MFC [коледбрекордвиев](../../mfc/reference/coledbrecordview-class.md). Объект представления записей, созданный из, `COleDBRecordView` позволяет отображать записи базы данных в элементах управления MFC. Представление записей является представлением диалогового окна, напрямую подключенным к OLE DB объекту набора строк, созданному из `CRowset` класса шаблона. Получение маркера для объекта набора строк является простым:

```cpp
COleDBRecordView myRecordView;
...
// CProductAccessor is a user record class
CRowset<CAccessor<CProductAccessor>> myRowSet = myRecordView.OnGetRowset();
```

Представление отображает поля `CRowset` объекта в элементах управления диалогового окна. `COleDBRecordView`Объект использует обмен данными диалоговых данных (DDX) и встроенные функции навигации `CRowset` ( `MoveFirst` ,, и `MoveNext` `MovePrev` `MoveLast` ) для автоматизации перемещения данных между элементами управления в форме и полями набора строк. `COleDBRecordView` отслеживает положение пользователя в наборе строк, чтобы представление записей мог обновить пользовательский интерфейс и [Предместит метод OnMove](../../mfc/reference/coledbrecordview-class.md#onmove) для обновления текущей записи перед переходом на другую.

С помощью функций DDX можно `COleDbRecordView` получать данные непосредственно из набора записей базы данных и отображать их в элементе управления диалогового окна. Используйте **DDX_** <strong>\*</strong> методы (такие как `DDX_Text` ), а не функции **DDX_Field** <strong>\*</strong> (такие как `DDX_FieldText` ) с `COleDbRecordView` .

## <a name="see-also"></a>См. также раздел

[Использование методов доступа](../../data/oledb/using-accessors.md)<br/>
[Класс Коледбрекордвиев](../../mfc/reference/coledbrecordview-class.md)<br/>
