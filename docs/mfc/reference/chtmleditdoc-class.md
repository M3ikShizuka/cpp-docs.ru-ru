---
description: 'Дополнительные сведения о: Чтмледитдок Class'
title: Класс Чтмледитдок
ms.date: 11/04/2016
f1_keywords:
- CHtmlEditDoc
- AFXHTML/CHtmlEditDoc
- AFXHTML/CHtmlEditDoc::CHtmlEditDoc
- AFXHTML/CHtmlEditDoc::GetView
- AFXHTML/CHtmlEditDoc::IsModified
- AFXHTML/CHtmlEditDoc::OpenURL
helpviewer_keywords:
- CHtmlEditDoc [MFC], CHtmlEditDoc
- CHtmlEditDoc [MFC], GetView
- CHtmlEditDoc [MFC], IsModified
- CHtmlEditDoc [MFC], OpenURL
ms.assetid: b2cca61f-e5d6-4099-b0d1-46bf85f0bd64
ms.openlocfilehash: 5fb8187ff7925efc5bdfa6a0079a8ec4b186ae63
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97115317"
---
# <a name="chtmleditdoc-class"></a>Класс Чтмледитдок

С помощью [CHtmlEditView](../../mfc/reference/chtmleditview-class.md)предоставляет функциональные возможности платформы редактирования WebBrowser в контексте архитектуры "документ — представление MFC".

## <a name="syntax"></a>Синтаксис

```
class AFX_NOVTABLE CHtmlEditDoc : public CDocument
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Чтмледитдок:: Чтмледитдок](#chtmleditdoc)|Формирует объект `CHtmlEditDoc`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Чтмледитдок:: View](#getview)|Извлекает `CHtmlEditView` объект, прикрепленный к этому документу.|
|[Чтмледитдок:: Modified](#ismodified)|Возвращает значение, указывающее, содержит ли элемент управления WebBrowser связанного представления документ, измененный пользователем.|
|[Чтмледитдок:: OpenURL](#openurl)|Открывает URL-адрес.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CDocument](../../mfc/reference/cdocument-class.md)

`CHtmlEditDoc`

## <a name="requirements"></a>Требования

**Заголовок:** afxhtml.h

## <a name="chtmleditdocchtmleditdoc"></a><a name="chtmleditdoc"></a> Чтмледитдок:: Чтмледитдок

Формирует объект `CHtmlEditDoc`.

```
CHtmlEditDoc();
```

## <a name="chtmleditdocgetview"></a><a name="getview"></a> Чтмледитдок:: View

Извлекает объект [CHtmlEditView](../../mfc/reference/chtmleditview-class.md) , прикрепленный к этому документу.

```
virtual CHtmlEditView* GetView() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на `CHtmlEditView` объект документа.

## <a name="chtmleditdocismodified"></a><a name="ismodified"></a> Чтмледитдок:: Modified

Возвращает значение, указывающее, содержит ли элемент управления WebBrowser связанного представления документ, измененный пользователем.

```
virtual BOOL IsModified();
```

## <a name="chtmleditdocopenurl"></a><a name="openurl"></a> Чтмледитдок:: OpenURL

Открывает URL-адрес.

```
virtual BOOL OpenURL(LPCTSTR lpszURL);
```

### <a name="parameters"></a>Параметры

*лпсзурл*<br/>
URL-адрес, который нужно открыть.

### <a name="return-value"></a>Возвращаемое значение

Возвращает TRUE при успешном выполнении, FALSE в случае сбоя.

## <a name="see-also"></a>См. также раздел

[Пример Хтмледит](../../overview/visual-cpp-samples.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)
