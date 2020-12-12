---
description: 'Дополнительные сведения о: CGopherFile Class'
title: Класс CGopherFile
ms.date: 11/04/2016
f1_keywords:
- CGopherFile
- AFXINET/CGopherFile
- AFXINET/CGopherFile::CGopherFile
helpviewer_keywords:
- CGopherFile [MFC], CGopherFile
ms.assetid: 3ca9898f-8cdb-4495-bbde-46d40100feda
ms.openlocfilehash: 8f511bdaf3ae6417972ea19465c0392832a2b408
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97184079"
---
# <a name="cgopherfile-class"></a>Класс CGopherFile

Обеспечивает возможность поиска и чтения файлов на сервере gopher.

> [!NOTE]
> Классы `CGopherConnection` ,, `CGopherFile` `CGopherFileFind` `CGopherLocator` и их члены являются устаревшими, так как они не работают на платформе Windows XP, но они продолжат работать на более ранних платформах.

## <a name="syntax"></a>Синтаксис

```
class CGopherFile : public CInternetFile
```

## <a name="members"></a>Члены

### <a name="protected-constructors"></a>Защищенные конструкторы

|Имя|Описание|
|----------|-----------------|
|[CGopherFile:: CGopherFile](#cgopherfile)|Формирует объект `CGopherFile`.|

## <a name="remarks"></a>Комментарии

Служба Gopher не разрешает пользователям записывать данные в файл gopher, так как эта служба в основном является интерфейсом, управляемым меню, для поиска информации. `CGopherFile`Функции элементов `Write` , `WriteString` и `Flush` не реализованы для `CGopherFile` . Вызов этих функций для `CGopherFile` объекта возвращает [кнотсуппортедексцептион](../../mfc/reference/cnotsupportedexception-class.md).

Дополнительные сведения о `CGopherFile` работе с другими классами Интернета MFC см. в статье Интернет – [программирование с помощью WinInet](../../mfc/win32-internet-extensions-wininet.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CFile](../../mfc/reference/cfile-class.md)

[CStdioFile](../../mfc/reference/cstdiofile-class.md)

[CInternetFile](../../mfc/reference/cinternetfile-class.md)

`CGopherFile`

## <a name="requirements"></a>Требования

**Заголовок:** афксинет. h

## <a name="cgopherfilecgopherfile"></a><a name="cgopherfile"></a> CGopherFile:: CGopherFile

Эта функция-член вызывается для создания `CGopherFile` объекта.

```
CGopherFile(
    HINTERNET hFile,
    CGopherLocator& refLocator,
    CGopherConnection* pConnection);

CGopherFile(
    HINTERNET hFile,
    HINTERNET hSession,
    LPCTSTR pstrLocator,
    DWORD dwLocLen,
    DWORD_PTR dwContext);
```

### <a name="parameters"></a>Параметры

*hFile*<br/>
Маркер для файла ХИНТЕРНЕТ.

*рефлокатор*<br/>
Ссылка на объект [кгоферлокатор](../../mfc/reference/cgopherlocator-class.md) .

*пконнектион*<br/>
Указатель на объект [кгоферконнектион](../../mfc/reference/cgopherconnection-class.md) .

*хсессион*<br/>
Маркер текущего сеанса Интернета.

*пстрлокатор*<br/>
Указатель на строку, используемую для нахождение сервера gopher. Дополнительные сведения о локаторах Gopher см. в статье о [сеансах Gopher](cgopherlocator-class.md) .

*двлоклен*<br/>
Значение типа DWORD, содержащее число байтов в *пстрлокатор*.

*двконтекст*<br/>
Указатель на идентификатор контекста открываемого файла.

### <a name="remarks"></a>Комментарии

Необходим `CGopherFile` объект для чтения из файла во время Интернет-сеанса Gopher.

Вы никогда не создаете `CGopherFile` объект напрямую. Вместо этого вызовите [кгоферконнектион:: OpenFile](../../mfc/reference/cgopherconnection-class.md#openfile) , чтобы открыть файл на сервере Gopher.

## <a name="see-also"></a>См. также раздел

[Класс Цинтернетфиле](../../mfc/reference/cinternetfile-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Цинтернетфиле](../../mfc/reference/cinternetfile-class.md)<br/>
[Класс Кгоферлокатор](../../mfc/reference/cgopherlocator-class.md)<br/>
[Класс Кгоферфилефинд](../../mfc/reference/cgopherfilefind-class.md)<br/>
[Класс Кгоферконнектион](../../mfc/reference/cgopherconnection-class.md)
