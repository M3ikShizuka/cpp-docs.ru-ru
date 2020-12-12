---
description: 'Дополнительные сведения о: структура CDaoTableDefInfo'
title: Структура CDaoTableDefInfo
ms.date: 11/04/2016
f1_keywords:
- CDaoTableDefInfo
helpviewer_keywords:
- CDaoTableDefInfo structure [MFC]
- DAO (Data Access Objects), TableDefs collection
ms.assetid: c01ccebb-5615-434e-883c-4f60eac943dd
ms.openlocfilehash: 953a255b35860dcce0ac8d3ef5081951dd15c344
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97247974"
---
# <a name="cdaotabledefinfo-structure"></a>Структура CDaoTableDefInfo

`CDaoTableDefInfo`Структура содержит сведения об объекте tabledef, определенном для объектов доступа к данным (DAO).

## <a name="syntax"></a>Синтаксис

```
struct CDaoTableDefInfo
{
    CString m_strName;               // Primary
    BOOL m_bUpdatable;               // Primary
    long m_lAttributes;              // Primary
    COleDateTime m_dateCreated;      // Secondary
    COleDateTime m_dateLastUpdated;  // Secondary
    CString m_strSrcTableName;       // Secondary
    CString m_strConnect;            // Secondary
    CString m_strValidationRule;     // All
    CString m_strValidationText;     // All
    long m_lRecordCount;             // All
};
```

#### <a name="parameters"></a>Параметры

*m_strName*<br/>
Уникально именует объект tabledef. Чтобы получить значение этого свойства напрямую, вызовите функцию члена [имени](../../mfc/reference/cdaotabledef-class.md#getname) объекта tabledef. Дополнительные сведения см. в разделе "свойство Name" справки DAO.

*m_bUpdatable*<br/>
Указывает, можно ли вносить изменения в таблицу. Чтобы определить, является ли таблица обновляемой, можно открыть `CDaoTableDef` объект для таблицы и вызвать функцию-член [канупдате](../../mfc/reference/cdaotabledef-class.md#canupdate) объекта. `CanUpdate` всегда возвращает ненулевое значение (TRUE) для вновь созданного объекта tabledef и значение 0 (FALSE) для присоединенного объекта tabledef. Новый объект TableDef может быть добавлен только в базу данных, для которой текущий пользователь имеет разрешение на запись. Если таблица содержит только необновляемые поля, функция `CanUpdate` возвращает 0. Если одно или несколько полей являются обновляемыми, `CanUpdate` возвращает ненулевое значение. Можно изменять только обновляемые поля. Дополнительные сведения см. в разделе "обновляемое свойство" справки DAO.

*m_lAttributes*<br/>
Задает характеристики таблицы, представленной объектом tabledef. Чтобы получить текущие атрибуты объекта tabledef, вызовите его функцию-член [OutAttribute](../../mfc/reference/cdaotabledef-class.md#getattributes) . Возвращаемое значение может быть сочетанием этих длинных констант (с помощью оператора побитового или (**&#124;**)):

- `dbAttachExclusive` Для баз данных, использующих ядро СУБД Microsoft Jet, указывает, что таблица является присоединенной таблицей, открытой для монопольного использования.

- `dbAttachSavePWD` Для баз данных, использующих ядро СУБД Microsoft Jet, указывает, что идентификатор пользователя и пароль для присоединенной таблицы сохраняются вместе со сведениями о соединении.

- `dbSystemObject` Указывает, что таблица является системной таблицей, предоставляемой ядром СУБД Microsoft Jet. (только для чтения).

- `dbHiddenObject` Указывает, что таблица является скрытой таблицей, предоставляемой ядром базы данных Microsoft Jet (для временного использования). (только для чтения).

- `dbAttachedTable` Указывает, что таблица является присоединенной таблицей из базы данных, отличной от ODBC, например базы данных Paradox.

- `dbAttachedODBC` Указывает, что таблица является присоединенной таблицей из базы данных ODBC, например Microsoft SQL Server.

*m_dateCreated*<br/>
Дата и время создания таблицы. Чтобы напрямую получить дату создания таблицы, вызовите функцию члена [жетдатекреатед](../../mfc/reference/cdaotabledef-class.md#getdatecreated) `CDaoTableDef` объекта, связанного с таблицей. Дополнительные сведения см. в комментариях ниже. Связанные сведения см. в подразделе «DateCreated, свойства LastUpdated» справки DAO.

*m_dateLastUpdated*<br/>
Дата и время последнего изменения, внесенного в структуру таблицы. Чтобы напрямую получить дату последнего обновления таблицы, вызовите функцию члена [жетдателаступдатед](../../mfc/reference/cdaotabledef-class.md#getdatelastupdated) `CDaoTableDef` объекта, связанного с таблицей. Дополнительные сведения см. в комментариях ниже. Связанные сведения см. в подразделе «DateCreated, свойства LastUpdated» справки DAO.

*m_strSrcTableName*<br/>
Указывает имя присоединенной таблицы, если таковое имеется. Чтобы напрямую получить имя исходной таблицы, вызовите функцию члена [жетсаурцетабленаме](../../mfc/reference/cdaotabledef-class.md#getsourcetablename) `CDaoTableDef` объекта, связанного с таблицей.

*m_strConnect*<br/>
Предоставляет сведения об источнике открытой базы данных. Это свойство можно проверить, вызвав функцию члена [соединения](../../mfc/reference/cdaotabledef-class.md#getconnect) `CDaoTableDef` GetObject объекта. Дополнительные сведения о строках подключения см. в разделе `GetConnect` .

*m_strValidationRule*<br/>
Значение, которое проверяет данные в полях tabledef по мере их изменения или добавления в таблицу. Проверка поддерживается только для баз данных, использующих ядро СУБД Microsoft Jet. Чтобы напрямую получить правило проверки, вызовите функцию члена [жетвалидатионруле](../../mfc/reference/cdaotabledef-class.md#getvalidationrule) `CDaoTableDef` объекта, связанного с таблицей. Связанные сведения см. в разделе "свойство ValidationRule" справки DAO.

*m_strValidationText*<br/>
Значение, указывающее текст сообщения, которое должно отображаться в приложении, если не удовлетворено правило проверки, заданное свойством ValidationRule. Связанные сведения см. в разделе «свойство Валидатионтекст» справки DAO.

*m_lRecordCount*<br/>
Число записей, к которым осуществлялось обращение в объекте tabledef. Этот параметр свойства доступен только для чтения. Чтобы напрямую получить число записей, вызовите функцию члена [жетрекордкаунт](../../mfc/reference/cdaotabledef-class.md#getrecordcount) `CDaoTableDef` объекта. Дополнительные сведения о `GetRecordCount` количестве записей см. в документации. Обратите внимание, что получение этого счетчика может быть трудоемкой операцией, если таблица содержит много записей.

## <a name="remarks"></a>Комментарии

Объект tabledef является объектом класса [кдаотабледеф](../../mfc/reference/cdaotabledef-class.md). Ссылки на первичный, вторичный и все вышеперечисленное указывают, как эта информация возвращается функцией-членом [жеттабледефинфо](../../mfc/reference/cdaodatabase-class.md#gettabledefinfo) в классе `CDaoDatabase` .

Сведения, получаемые функцией-членом [CDaoDatabase:: жеттабледефинфо](../../mfc/reference/cdaodatabase-class.md#gettabledefinfo) , хранятся в `CDaoTableDefInfo` структуре. Вызовите `GetTableDefInfo` функцию-член `CDaoDatabase` объекта в коллекции TableDefs, в которой хранится объект tabledef. `CDaoTableDefInfo` также определяет `Dump` функцию-член в отладочных сборках. Можно использовать `Dump` для дампа содержимого `CDaoTableDefInfo` объекта.

Параметры даты и времени производятся на основе компьютера, на котором была создана или обновлена базовая таблица. В многопользовательской среде пользователи должны получить эти параметры непосредственно с файлового сервера, чтобы избежать расхождений в параметрах свойств DateCreated и LastUpdated.

## <a name="requirements"></a>Требования

**Заголовок:** афксдао. h

## <a name="see-also"></a>См. также раздел

[Структуры, стили, обратные вызовы и схемы сообщений](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[Класс Кдаотабледеф](../../mfc/reference/cdaotabledef-class.md)<br/>
[Класс CDaoDatabase](../../mfc/reference/cdaodatabase-class.md)
