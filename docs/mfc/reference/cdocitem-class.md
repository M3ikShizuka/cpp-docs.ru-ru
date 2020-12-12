---
description: 'Дополнительные сведения о: КдоЦитем Class'
title: Класс КдоЦитем
ms.date: 11/04/2016
f1_keywords:
- CDocItem
- AFXOLE/CDocItem
- AFXOLE/CDocItem::GetDocument
- AFXOLE/CDocItem::IsBlank
helpviewer_keywords:
- CDocItem [MFC], GetDocument
- CDocItem [MFC], IsBlank
ms.assetid: 84fb8610-a4c8-4211-adc0-e70e8d002c11
ms.openlocfilehash: 9e126d4351248165a3961739c13cc6ce7330c10c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97185145"
---
# <a name="cdocitem-class"></a>Класс КдоЦитем

Базовый класс для элементов документа, являющихся компонентами данных документа.

## <a name="syntax"></a>Синтаксис

```
class CDocItem : public CCmdTarget
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[КдоЦитем:: a Document](#getdocument)|Возвращает документ, содержащий элемент.|
|[КдоЦитем:: Blank](#isblank)|Определяет, содержит ли элемент какие бы то ни было сведения.|

## <a name="remarks"></a>Комментарии

`CDocItem` объекты используются для представления элементов OLE как в клиентских, так и в серверных документах.

Дополнительные сведения см. в разделе [контейнеры статьи: Реализация контейнера](../../mfc/containers-implementing-a-container.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

`CDocItem`

## <a name="requirements"></a>Требования

**Заголовок:** афксоле. h

## <a name="cdocitemgetdocument"></a><a name="getdocument"></a> КдоЦитем:: a Document

Вызовите эту функцию, чтобы получить документ, содержащий элемент.

```
CDocument* GetDocument() const;
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на документ, содержащий элемент; Значение NULL, если элемент не является частью документа.

### <a name="remarks"></a>Комментарии

Эта функция переопределяется в производных классах [COleClientItem](../../mfc/reference/coleclientitem-class.md) и [COleServerItem](../../mfc/reference/coleserveritem-class.md), возвращая указатель либо на [коледокумент](../../mfc/reference/coledocument-class.md), [колелинкингдок](../../mfc/reference/colelinkingdoc-class.md), либо на объект [колесервердок](../../mfc/reference/coleserverdoc-class.md) .

## <a name="cdocitemisblank"></a><a name="isblank"></a> КдоЦитем:: Blank

Вызывается платформой при сериализации по умолчанию.

```
virtual BOOL IsBlank() const;
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если элемент не содержит сведений; в противном случае — 0.

### <a name="remarks"></a>Комментарии

По умолчанию `CDocItem` объекты не являются пустыми. Объекты [COleClientItem](../../mfc/reference/coleclientitem-class.md) иногда являются пустыми, так как они наследуются непосредственно от `CDocItem` . Однако объекты [COleServerItem](../../mfc/reference/coleserveritem-class.md) всегда пусты. По умолчанию приложения OLE `COleClientItem` , содержащие объекты, не имеющие экстента x или y, сериализуются. Это делается путем возврата значения TRUE из переопределения, `IsBlank` Если у элемента нет экстента x или y.

Переопределите эту функцию, если требуется реализовать другие действия во время сериализации.

## <a name="see-also"></a>См. также раздел

[Класс от CCmdTarget](../../mfc/reference/ccmdtarget-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Коледокумент](../../mfc/reference/coledocument-class.md)<br/>
[Класс COleServerItem](../../mfc/reference/coleserveritem-class.md)<br/>
[Класс COleClientItem](../../mfc/reference/coleclientitem-class.md)
