---
description: 'Дополнительные сведения о: Ккачеддатапаспроперти Class'
title: Класс Ккачеддатапаспроперти
ms.date: 11/04/2016
f1_keywords:
- CCachedDataPathProperty
- AFXCTL/CCachedDataPathProperty
- AFXCTL/CCachedDataPathProperty::CCachedDataPathProperty
- AFXCTL/CCachedDataPathProperty::m_Cache
helpviewer_keywords:
- CCachedDataPathProperty [MFC], CCachedDataPathProperty
- CCachedDataPathProperty [MFC], m_Cache
ms.assetid: 0d81356b-4fe5-43f6-aed2-2eb5a5485706
ms.openlocfilehash: a61d2553afc4415da29399293843deb1be5f113d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97122503"
---
# <a name="ccacheddatapathproperty-class"></a>Класс Ккачеддатапаспроперти

Реализует свойство элемента управления OLE, асинхронно переданного и кэшированного в файле памяти.

## <a name="syntax"></a>Синтаксис

```
class CCachedDataPathProperty : public CDataPathProperty
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккачеддатапаспроперти:: Ккачеддатапаспроперти](#ccacheddatapathproperty)|Формирует объект `CCachedDataPathProperty`.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Ккачеддатапаспроперти:: m_Cache](#m_cache)|`CMemFile` Объект, в котором кэшируются данные.|

## <a name="remarks"></a>Комментарии

Файл памяти хранится в ОЗУ, а не на диске, и его удобно использовать для быстрой временной передачи.

Наряду с `CAysncMonikerFile` и `CDataPathProperty` `CCachedDataPathProperty` предоставляет функциональные возможности для использования асинхронных моникеров в элементах управления OLE. С помощью `CCachedDataPathProperty` объектов можно асинхронно передавать данные из URL-адреса или из источника файла и сохранять их в файле памяти через `m_Cache` общую переменную. Все данные хранятся в файле памяти, и нет необходимости переопределять [ондатааваилабле](../../mfc/reference/casyncmonikerfile-class.md#ondataavailable) , если вы не хотите отслеживать уведомления и отвечать на них. Например, при передаче большого размера. GIF-файл и хочу уведомить свой элемент управления о том, что поступило больше данных, и должен перерисовывать себя, переопределите, `OnDataAvailable` чтобы сделать уведомление.

Класс `CCachedDataPathProperty` является производным от `CDataPathProperty` .

Дополнительные сведения об использовании асинхронных моникеров и элементов управления ActiveX в веб – приложениях см. в следующих разделах:

- [Первые действия в Интернете: элементы управления ActiveX](../../mfc/activex-controls-on-the-internet.md)

- [Первые действия через Интернет: асинхронные моникеры](../../mfc/asynchronous-monikers-on-the-internet.md)

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CFile](../../mfc/reference/cfile-class.md)

[COleStreamFile](../../mfc/reference/colestreamfile-class.md)

[CMonikerFile](../../mfc/reference/cmonikerfile-class.md)

[CAsyncMonikerFile](../../mfc/reference/casyncmonikerfile-class.md)

[CDataPathProperty](../../mfc/reference/cdatapathproperty-class.md)

`CCachedDataPathProperty`

## <a name="requirements"></a>Требования

**Заголовок:** afxctl. h

## <a name="ccacheddatapathpropertyccacheddatapathproperty"></a><a name="ccacheddatapathproperty"></a> Ккачеддатапаспроперти:: Ккачеддатапаспроперти

Формирует объект `CCachedDataPathProperty`.

```
CCachedDataPathProperty(COleControl* pControl = NULL);

CCachedDataPathProperty(
    LPCTSTR lpszPath,
    COleControl* pControl = NULL);
```

### <a name="parameters"></a>Параметры

*pControl*<br/>
Указатель на объект элемента управления ActiveX, который должен быть связан с этим `CCachedDataPathProperty` объектом.

*лпсзпас*<br/>
Путь, который может быть абсолютным или относительным, используется для создания асинхронного моникера, который ссылается на фактическое абсолютное расположение свойства. `CCachedDataPathProperty` использует URL-адреса, а не имена файлов. Если требуется `CCachedDataPathProperty` объект для файла, добавьте в начало file://путь.

### <a name="remarks"></a>Комментарии

`COleControl`Объект, на который указывает *пконтрол* , используется [открытыми](../../mfc/reference/cdatapathproperty-class.md#open) и извлеченными производными классами. Если *пконтрол* имеет значение null, то элемент управления, используемый с, `Open` должен быть задан с помощью [сетконтрол](../../mfc/reference/cdatapathproperty-class.md#setcontrol). Если *лпсзпас* имеет значение null, можно передать путь через `Open` или задать его с помощью [сетпас](../../mfc/reference/cdatapathproperty-class.md#setpath).

## <a name="ccacheddatapathpropertym_cache"></a><a name="m_cache"></a> Ккачеддатапаспроперти:: m_Cache

Содержит имя класса файла памяти, в который кэшируются данные.

```
CMemFile m_Cache;
```

### <a name="remarks"></a>Комментарии

Файл памяти хранится в ОЗУ, а не на диске.

## <a name="see-also"></a>См. также раздел

[Класс Кдатапаспроперти](../../mfc/reference/cdatapathproperty-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Кдатапаспроперти](../../mfc/reference/cdatapathproperty-class.md)
