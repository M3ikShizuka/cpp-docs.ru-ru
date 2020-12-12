---
description: 'Дополнительные сведения о: структура CDaoRelationFieldInfo'
title: Структура CDaoRelationFieldInfo
ms.date: 11/04/2016
f1_keywords:
- CDaoRelationFieldInfo
helpviewer_keywords:
- DAO (Data Access Objects), Relations collection
- CDaoRelationFieldInfo structure [MFC]
ms.assetid: 47cb89ca-dc80-47ce-96fd-cc4b88512558
ms.openlocfilehash: eb470752a9e9da5f610dd59976f2716fa1c4e18a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97248168"
---
# <a name="cdaorelationfieldinfo-structure"></a>Структура CDaoRelationFieldInfo

`CDaoRelationFieldInfo`Структура содержит сведения о поле в связи, определенном для объектов доступа к данным (DAO).

## <a name="syntax"></a>Синтаксис

```
struct CDaoRelationFieldInfo
{
    CString m_strName;           // Primary
    CString m_strForeignName;    // Primary
};
```

#### <a name="parameters"></a>Параметры

*m_strName*<br/>
Имя поля в основной таблице связи.

*m_strForeignName*<br/>
Имя поля во внешней таблице связи.

## <a name="remarks"></a>Комментарии

Объект DAO relation определяет поля в основной таблице и поля во внешней таблице, определяющей отношение. Ссылки на основные в определении структуры выше указывают, как эти сведения возвращаются в элементе `m_pFieldInfos` объекта [CDaoRelationInfo](../../mfc/reference/cdaorelationinfo-structure.md) , полученном путем вызова функции-члена [жетрелатионинфо](../../mfc/reference/cdaodatabase-class.md#getrelationinfo) класса `CDaoDatabase` .

Объекты отношений и объекты полей отношений не представлены классом MFC. Вместо этого объекты DAO базовых объектов MFC класса [CDaoDatabase](../../mfc/reference/cdaodatabase-class.md) содержат коллекцию объектов отношений, называемую коллекцией связей. Каждый объект связи, в свою очередь, содержит коллекцию объектов полей связи. Каждый объект поля связи сопоставляет поле в основной таблице с полем во внешней таблице. Вместе объекты полей связи определяют группу полей в каждой таблице, которые вместе определяют связь. `CDaoDatabase` позволяет получить доступ к объектам отношений с помощью `CDaoRelationInfo` объекта, вызвав `GetRelationInfo` функцию-член. `CDaoRelationInfo`Затем объект содержит элемент данных, `m_pFieldInfos` указывающий на массив `CDaoRelationFieldInfo` объектов.

Вызовите функцию-член [жетрелатионинфо](../../mfc/reference/cdaodatabase-class.md#getrelationinfo) содержащего `CDaoDatabase` объекта, в коллекции связей которого хранится интересующий вас объект отношения. Затем получите доступ к `m_pFieldInfos` члену объекта [CDaoRelationInfo](../../mfc/reference/cdaorelationinfo-structure.md) . `CDaoRelationFieldInfo` также определяет `Dump` функцию-член в отладочных сборках. Можно использовать `Dump` для дампа содержимого `CDaoRelationFieldInfo` объекта.

## <a name="requirements"></a>Требования

**Заголовок:** афксдао. h

## <a name="see-also"></a>См. также раздел

[Структуры, стили, обратные вызовы и схемы сообщений](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[Структура CDaoRelationInfo](../../mfc/reference/cdaorelationinfo-structure.md)
