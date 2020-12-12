---
description: 'Дополнительные сведения о: Карчивиксцептион Class'
title: Класс Карчивиксцептион
ms.date: 11/04/2016
f1_keywords:
- CArchiveException
- AFX/CArchiveException
- AFX/CArchiveException::CArchiveException
- AFX/CArchiveException::m_cause
- AFX/CArchiveException::m_strFileName
helpviewer_keywords:
- CArchiveException [MFC], CArchiveException
- CArchiveException [MFC], m_cause
- CArchiveException [MFC], m_strFileName
ms.assetid: da31a127-e86c-41d1-b0b6-bed0865b1b49
ms.openlocfilehash: ce8355583e0a7a3fd8a382873a0e4b2a1ea91b83
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97185405"
---
# <a name="carchiveexception-class"></a>Класс Карчивиксцептион

Представляет условие исключения сериализации

## <a name="syntax"></a>Синтаксис

```
class CArchiveException : public CException
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Карчивиксцептион:: Карчивиксцептион](#carchiveexception)|Формирует объект `CArchiveException`.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Карчивиксцептион:: m_cause](#m_cause)|Указывает причину исключения.|
|[Карчивиксцептион:: m_strFileName](#m_strfilename)|Указывает имя файла для этого условия исключения.|

## <a name="remarks"></a>Комментарии

`CArchiveException`Класс включает открытый элемент данных, указывающий причину исключения.

`CArchiveException` объекты создаются и создаются в функциях элементов [CArchive](../../mfc/reference/carchive-class.md) . Доступ к этим объектам можно получить в области выражения **catch** . Код причины не зависит от операционной системы. Дополнительные сведения об обработке исключений см. в разделе [обработка исключений (MFC)](../../mfc/exception-handling-in-mfc.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CException](../../mfc/reference/cexception-class.md)

`CArchiveException`

## <a name="requirements"></a>Требования

**Заголовок:** AFX. h

## <a name="carchiveexceptioncarchiveexception"></a><a name="carchiveexception"></a> Карчивиксцептион:: Карчивиксцептион

Конструирует `CArchiveException` объект, сохраняя значение *причины* в объекте.

```
CArchiveException(
    int cause = CArchiveException::none,
    LPCTSTR lpszArchiveName = NULL);
```

### <a name="parameters"></a>Параметры

*cause*<br/>
Переменная перечислимого типа, указывающая причину исключения. Список перечислителей см. в разделе элемент данных [m_cause](#m_cause) .

*лпсзарчивенаме*<br/>
Указывает на строку, содержащую имя `CArchive` объекта, вызвавшего исключение.

### <a name="remarks"></a>Комментарии

Вы можете создать `CArchiveException` объект в куче и вызвать его самостоятельно или позволить глобальной функции [афкссроварчивиксцептион](../../mfc/reference/exception-processing.md#afxthrowarchiveexception) его обработку.

Не используйте этот конструктор напрямую; Вместо этого вызовите глобальную функцию `AfxThrowArchiveException` .

## <a name="carchiveexceptionm_cause"></a><a name="m_cause"></a> Карчивиксцептион:: m_cause

Указывает причину исключения.

```
int m_cause;
```

### <a name="remarks"></a>Комментарии

Этот элемент данных является открытой переменной типа **`int`** . Его значения определяются `CArchiveException` перечисляемым типом. Перечислители и их значение представлено далее.

- `CArchiveException::none` Ошибки не обнаружены.

- `CArchiveException::genericException` Неопределенная ошибка.

- `CArchiveException::readOnly` Попытка записи в архив, Открытый для загрузки.

- `CArchiveException::endOfFile` Достигнут конец файла при чтении объекта.

- `CArchiveException::writeOnly` Попытка чтения из архива, открытого для хранения.

- `CArchiveException::badIndex` Недопустимый формат файла.

- `CArchiveException::badClass` Попытка чтения объекта в объект неправильного типа.

- `CArchiveException::badSchema` Попытка чтения объекта с другой версией класса.

    > [!NOTE]
    >  Перечислители причины `CArchiveException` отличаются от перечислителей причины `CFileException`.

    > [!NOTE]
    > Параметр `CArchiveException::generic` использовать не рекомендуется. Взамен рекомендуется использовать `genericException`. Если **универсальное** приложение используется в приложении и строится с помощью параметра/CLR, то будут отображаться синтаксические ошибки, которые непросто расшифровать.

## <a name="carchiveexceptionm_strfilename"></a><a name="m_strfilename"></a> Карчивиксцептион:: m_strFileName

Указывает имя файла для этого условия исключения.

```
CString m_strFileName;
```

## <a name="see-also"></a>См. также раздел

[Класс CException](../../mfc/reference/cexception-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс CArchive](../../mfc/reference/carchive-class.md)<br/>
[AfxThrowArchiveException](../../mfc/reference/exception-processing.md#afxthrowarchiveexception)<br/>
[Обработка исключений](../../mfc/reference/exception-processing.md)
