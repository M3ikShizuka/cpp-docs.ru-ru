---
description: 'Дополнительные сведения о: структура Кдаопараметеринфо'
title: Структура CDaoParameterInfo
ms.date: 09/17/2019
f1_keywords:
- CDaoParameterInfo
helpviewer_keywords:
- CDaoParameterInfo structure [MFC]
- DAO (Data Access Objects), Parameters collection
ms.assetid: 45fd53cd-cb84-4e12-b48d-7f2979f898ad
ms.openlocfilehash: b4cd1916bb30c3b646e9b0892e2bdcdf5ade30b4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97250727"
---
# <a name="cdaoparameterinfo-structure"></a>Структура CDaoParameterInfo

`CDaoParameterInfo`Структура содержит сведения об объекте параметра, определенном для объектов доступа к данным (DAO). Версия DAO 3,6 является окончательной и считается устаревшей.

## <a name="syntax"></a>Синтаксис

```
struct CDaoParameterInfo
{
    CString m_strName;       // Primary
    short m_nType;           // Primary
    ColeVariant m_varValue;  // Secondary
};
```

#### <a name="parameters"></a>Параметры

*m_strName*<br/>
Уникально именует объект параметра. Дополнительные сведения см. в разделе "свойство Name" справки DAO.

*m_nType*<br/>
Значение типа, указывающее тип данных объекта параметра. Список возможных значений см. в описании элемента *m_nType* структуры [CDaoFieldInfo](../../mfc/reference/cdaofieldinfo-structure.md) . Дополнительные сведения см. в разделе "свойство Type" справки DAO.

*m_varValue*<br/>
Значение параметра, хранящееся в объекте [COleVariant](../../mfc/reference/colevariant-class.md) .

## <a name="remarks"></a>Комментарии

Ссылки на первичный и вторичный выше указывают, как эта информация возвращается функцией-членом [GetParameterInfo](../../mfc/reference/cdaoquerydef-class.md#getparameterinfo) в классе `CDaoQueryDef` .

MFC не инкапсулирует объекты параметров DAO в классе. Объекты DAO QueryDef. базовые `CDaoQueryDef` объекты MFC хранят параметры в коллекциях параметров. Чтобы получить доступ к объектам параметров в объекте [кдаокуеридеф](../../mfc/reference/cdaoquerydef-class.md) , вызовите функцию-член объекта QueryDef `GetParameterInfo` для определенного имени параметра или индекса в коллекции Parameters. Вы можете использовать функцию-член [кдаокуеридеф:: GetParameterCount](../../mfc/reference/cdaoquerydef-class.md#getparametercount) в сочетании с `GetParameterInfo` , чтобы прокручивать коллекцию Parameters.

Сведения, получаемые функцией-членом [кдаокуеридеф:: GetParameterInfo](../../mfc/reference/cdaoquerydef-class.md#getparameterinfo) , хранятся в `CDaoParameterInfo` структуре. Вызовите `GetParameterInfo` объект QueryDef, в коллекции параметров которого хранится объект Parameter.

> [!NOTE]
> Если необходимо получить или задать только значение параметра, используйте функции-члены [жетпарамвалуе](../../mfc/reference/cdaorecordset-class.md#getparamvalue) и [сетпарамвалуе](../../mfc/reference/cdaorecordset-class.md#setparamvalue) класса `CDaoRecordset` .

`CDaoParameterInfo` также определяет `Dump` функцию-член в отладочных сборках. Можно использовать `Dump` для дампа содержимого `CDaoParameterInfo` объекта.

## <a name="requirements"></a>Требования

**Заголовок:** афксдао. h

## <a name="see-also"></a>См. также раздел

[Структуры, стили, обратные вызовы и схемы сообщений](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[Класс Кдаокуеридеф](../../mfc/reference/cdaoquerydef-class.md)
