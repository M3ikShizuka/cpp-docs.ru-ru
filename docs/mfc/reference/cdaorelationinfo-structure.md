---
description: 'Дополнительные сведения о: структура CDaoRelationInfo'
title: Структура CDaoRelationInfo
ms.date: 06/25/2018
f1_keywords:
- CDaoRelationInfo
helpviewer_keywords:
- DAO (Data Access Objects), Relations collection
- CDaoRelationInfo structure [MFC]
ms.assetid: 92dda090-fe72-4090-84ec-429498a48aad
ms.openlocfilehash: efcc880d30dd18108005d9c4f265238b81551532
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97222246"
---
# <a name="cdaorelationinfo-structure"></a>Структура CDaoRelationInfo

`CDaoRelationInfo`Структура содержит сведения о связи, определенной между полями двух таблиц в объекте [CDaoDatabase](../../mfc/reference/cdaodatabase-class.md) .

## <a name="syntax"></a>Синтаксис

```cpp
struct CDaoRelationInfo
{
    CDaoRelationInfo();                     // Constructor
    CString m_strName;                      // Primary
    CString m_strTable;                     // Primary
    CString m_strForeignTable;              // Primary
    long m_lAttributes;                     // Secondary
    CDaoRelationFieldInfo* m_pFieldInfos;   // Secondary
    short m_nFields;                        // Secondary
    // Below the // Implementation comment:
    // Destructor, not otherwise documented
};
```

#### <a name="parameters"></a>Параметры

*m_strName*<br/>
Уникально именует объект связи. Дополнительные сведения см. в разделе "свойство Name" справки DAO.

*m_strTable*<br/>
Присваивает имя основной таблице в отношении.

*m_strForeignTable*<br/>
Называет внешнюю таблицу в отношении. Внешняя таблица — это таблица, используемая для хранения внешних ключей. Как правило, внешняя таблица используется для установления или принудительного применения ссылочной целостности. Внешняя таблица обычно находится на стороне «многие» связи «один ко многим». Примерами внешних таблиц являются таблицы, содержащие коды для Штатов Америки или канадских районов или заказов клиентов.

*m_lAttributes*<br/>
Содержит сведения о типе связи. Значение этого элемента может быть любым из следующих:

- `dbRelationUnique` Отношение "один к одному".

- `dbRelationDontEnforce` Связь не применяется (без ссылочной целостности).

- `dbRelationInherited` Связь существует в нетекущей базе данных, содержащей две соединяемые таблицы.

- `dbRelationLeft` Связь является левым соединением. Левое внешнее соединение включает все записи из первой (левой) двух таблиц, даже если нет совпадающих значений для записей во второй (правой) таблице.

- `dbRelationRight` Связь является правильным соединением. Правое внешнее соединение включает все записи из второй (правого) двух таблиц, даже если нет совпадающих значений для записей в первой (левой) таблице.

- `dbRelationUpdateCascade` Обновления будут каскадными.

- `dbRelationDeleteCascade` Удаления будут каскадными.

*m_pFieldInfos*<br/>
Указатель на массив структур [CDaoRelationFieldInfo](../../mfc/reference/cdaorelationfieldinfo-structure.md) . Массив содержит по одному объекту для каждого поля в связи. `m_nFields`Элемент данных предоставляет число элементов массива.

*m_nFields*<br/>
Число `CDaoRelationFieldInfo` объектов в элементе `m_pFieldInfos` данных.

## <a name="remarks"></a>Комментарии

Ссылки на первичный и вторичный выше указывают, как эта информация возвращается функцией-членом [жетрелатионинфо](../../mfc/reference/cdaodatabase-class.md#getrelationinfo) в классе `CDaoDatabase` .

Объекты отношений не представлены классом MFC. Вместо этого объект DAO, лежащий в основе объекта MFC `CDaoDatabase` класса, поддерживает коллекцию объектов relation: `CDaoDatabase` предоставляет функции-члены для доступа к некоторым отдельным элементам сведений о связях или к ним можно получить доступ сразу с помощью `CDaoRelationInfo` объекта, вызвав функцию- `GetRelationInfo` член содержащего объекта базы данных.

Сведения, получаемые функцией-членом [CDaoDatabase:: жетрелатионинфо](../../mfc/reference/cdaodatabase-class.md#getrelationinfo) , хранятся в `CDaoRelationInfo` структуре. `CDaoRelationInfo` также определяет `Dump` функцию-член в отладочных сборках. Можно использовать `Dump` для дампа содержимого `CDaoRelationInfo` объекта.

## <a name="requirements"></a>Требования

**Заголовок:** афксдао. h

## <a name="see-also"></a>См. также раздел

[Структура CDaoRelationFieldInfo](../../mfc/reference/cdaorelationfieldinfo-structure.md)
