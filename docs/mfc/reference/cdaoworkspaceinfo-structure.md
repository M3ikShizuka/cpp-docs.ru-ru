---
description: 'Дополнительные сведения о: структура Кдаоворкспацеинфо'
title: Структура CDaoWorkspaceInfo
ms.date: 11/04/2016
f1_keywords:
- CDaoWorkspaceInfo
helpviewer_keywords:
- CDaoWorkspaceInfo structure [MFC]
- DAO (Data Access Objects), Workspaces collection
ms.assetid: a1f4b25e-f9c6-4196-b075-d1df99c54124
ms.openlocfilehash: b89e8787c2103244535e9458650f1f104478b748
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97222207"
---
# <a name="cdaoworkspaceinfo-structure"></a>Структура CDaoWorkspaceInfo

`CDaoWorkspaceInfo`Структура содержит сведения о рабочей области, определенной для доступа к базе данных объектов доступа к данным (DAO).

## <a name="syntax"></a>Синтаксис

```
struct CDaoWorkspaceInfo
{
    CString m_strName;           // Primary
    CString m_strUserName;       // Secondary
    BOOL m_bIsolateODBCTrans;    // All
};
```

#### <a name="parameters"></a>Параметры

*m_strName*<br/>
Уникально именует объект рабочей области. Чтобы получить значение этого свойства напрямую, вызовите [функцию члена "GetObject" объекта QueryDef](../../mfc/reference/cdaoquerydef-class.md#getname) . Дополнительные сведения см. в разделе "свойство Name" справки DAO.

*m_strUserName*<br/>
Значение, представляющее владельца объекта рабочей области. Связанные сведения см. в разделе "свойство UserName" справки DAO.

*m_bIsolateODBCTrans*<br/>
Значение, указывающее, изолированы ли несколько транзакций, использующих одну и ту же базу данных ODBC. Дополнительные сведения см. в разделе [кдаоворкспаце:: сетисолатеодбктранс](../../mfc/reference/cdaoworkspace-class.md#setisolateodbctrans). Связанные сведения см. в разделе «свойство Исолатеодбктранс» справки DAO.

## <a name="remarks"></a>Комментарии

Рабочая область — это объект класса [кдаоворкспаце](../../mfc/reference/cdaoworkspace-class.md). Ссылки на первичный, вторичный и все вышеперечисленное указывают, как эта информация возвращается функцией-членом [жетворкспацеинфо](../../mfc/reference/cdaoworkspace-class.md#getworkspaceinfo) в классе `CDaoWorkspace` .

Сведения, получаемые функцией-членом [кдаоворкспаце:: жетворкспацеинфо](../../mfc/reference/cdaoworkspace-class.md#getworkspaceinfo) , хранятся в `CDaoWorkspaceInfo` структуре. `CDaoWorkspaceInfo` также определяет `Dump` функцию-член в отладочных сборках. Можно использовать `Dump` для дампа содержимого `CDaoWorkspaceInfo` объекта.

## <a name="requirements"></a>Требования

**Заголовок:** афксдао. h

## <a name="see-also"></a>См. также раздел

[Структуры, стили, обратные вызовы и схемы сообщений](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[Класс Кдаоворкспаце](../../mfc/reference/cdaoworkspace-class.md)
