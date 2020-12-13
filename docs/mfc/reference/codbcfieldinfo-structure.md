---
description: 'Дополнительные сведения о: структура Кодбкфиелдинфо'
title: Структура CODBCFieldInfo
ms.date: 11/04/2016
f1_keywords:
- CODBCFieldInfo
helpviewer_keywords:
- ODBC [MFC], data source information
- CODBCFieldInfo structure [MFC]
ms.assetid: 92598b4f-facc-4108-b282-63a179ff79ab
ms.openlocfilehash: 7cd7072719bec46cfbfaeb02c5c86d714c4de13c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331412"
---
# <a name="codbcfieldinfo-structure"></a>Структура CODBCFieldInfo

`CODBCFieldInfo`Структура содержит сведения о полях в источнике данных ODBC.

## <a name="syntax"></a>Синтаксис

```
struct CODBCFieldInfo
{
    CString m_strName;
    SWORD m_nSQLType;
    UDWORD m_nPrecision;
    SWORD m_nScale;
    SWORD m_nNullability;
};
```

#### <a name="parameters"></a>Параметры

*m_strName*<br/>
Имя поля.

*m_nSQLType*<br/>
Тип данных SQL поля. Это может быть тип данных ODBC SQL или тип данных SQL, зависящий от драйвера. Список допустимых типов данных ODBC SQL см. в разделе "типы данных SQL" в Windows SDK. Дополнительные сведения о типах данных SQL, относящихся к драйверам, см. в документации по драйверу.

*m_nPrecision*<br/>
Максимальная точность поля. Дополнительные сведения см. в разделе "точность, масштаб, Длина и размер дисплея" в Windows SDK.

*m_nScale*<br/>
Масштаб поля. Дополнительные сведения см. в разделе "точность, масштаб, Длина и размер дисплея" в Windows SDK.

*m_nNullability*<br/>
Принимает ли поле значение null. Это может быть одно из двух значений: SQL_NULLABLE, если поле принимает значения NULL, или SQL_NO_NULLS, если поле не принимает значения NULL.

## <a name="remarks"></a>Комментарии

Чтобы получить эти сведения, вызовите метод [CRecordset:: жетодбкфиелдинфо](../../mfc/reference/crecordset-class.md#getodbcfieldinfo).

## <a name="requirements"></a>Требования

**Заголовок:** афксдб. h

## <a name="see-also"></a>См. также раздел

[Структуры, стили, обратные вызовы и схемы сообщений](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[CRecordset:: Жетодбкфиелдинфо](../../mfc/reference/crecordset-class.md#getodbcfieldinfo)<br/>
[CRecordset:: GetFieldValue](../../mfc/reference/crecordset-class.md#getfieldvalue)
