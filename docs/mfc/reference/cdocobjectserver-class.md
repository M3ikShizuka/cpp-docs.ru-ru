---
description: 'Дополнительные сведения о: Кдокобжектсервер Class'
title: Класс Кдокобжектсервер
ms.date: 09/12/2018
f1_keywords:
- CDocObjectServer
- AFXDOCOB/CDocObjectServer
- AFXDOCOB/CDocObjectServer::CDocObjectServer
- AFXDOCOB/CDocObjectServer::ActivateDocObject
- AFXDOCOB/CDocObjectServer::OnActivateView
- AFXDOCOB/CDocObjectServer::OnApplyViewState
- AFXDOCOB/CDocObjectServer::OnSaveViewState
helpviewer_keywords:
- CDocObjectServer [MFC], CDocObjectServer
- CDocObjectServer [MFC], ActivateDocObject
- CDocObjectServer [MFC], OnActivateView
- CDocObjectServer [MFC], OnApplyViewState
- CDocObjectServer [MFC], OnSaveViewState
ms.assetid: 18cd0dff-0616-4472-b8d9-66c081bc383a
ms.openlocfilehash: 5a87363fef66a4819fc8efd504da96398cf3c89e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97184950"
---
# <a name="cdocobjectserver-class"></a>Класс Кдокобжектсервер

Реализует дополнительные интерфейсы OLE, необходимые для преобразования стандартного сервера `COleDocument` в полноценный сервер DocObject: `IOleDocument`, `IOleDocumentView`, `IOleCommandTarget`и `IPrint`.

## <a name="syntax"></a>Синтаксис

```
class CDocObjectServer : public CCmdTarget
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кдокобжектсервер:: Кдокобжектсервер](#cdocobjectserver)|Формирует объект `CDocObjectServer`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кдокобжектсервер:: Активатедокобжект](#activatedocobject)|Активирует сервер объектов документов, но не отображает его.|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[Кдокобжектсервер:: Онактиватевиев](#onactivateview)|Отображает представление DocObject.|
|[Кдокобжектсервер:: Онаппливиевстате](#onapplyviewstate)|Восстанавливает состояние представления DocObject.|
|[Кдокобжектсервер:: Онсавевиевстате](#onsaveviewstate)|Сохраняет состояние представления DocObject.|

## <a name="remarks"></a>Комментарии

`CDocObjectServer` является производным от `CCmdTarget` и тесно взаимодействует с `COleServerDoc` интерфейсами.

Документ сервера DocObject может содержать объекты [кдокобжектсерверитем](../../mfc/reference/cdocobjectserveritem-class.md) , представляющие интерфейс сервера для DocObject элементов.

Чтобы настроить сервер DocObject, создайте класс, производный от класса, `CDocObjectServer` и переопределите его функции настройки представления, [онактиватевиев](#onactivateview), [онаппливиевстате](#onapplyviewstate)и [онсавевиевстате](#onsaveviewstate). Необходимо будет предоставить новый экземпляр класса в ответ на вызовы платформы.

Дополнительные сведения о Докобжектс см. в разделе [кдокобжектсерверитем](../../mfc/reference/cdocobjectserveritem-class.md) и [колекмдуи](../../mfc/reference/colecmdui-class.md) в *справочнике по MFC*.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

`CDocObjectServer`

## <a name="requirements"></a>Требования

**Заголовок:** афксдокоб. h

## <a name="cdocobjectserveractivatedocobject"></a><a name="activatedocobject"></a> Кдокобжектсервер:: Активатедокобжект

Вызовите эту функцию, чтобы активировать (но не показывать) сервер объектов Document.

```cpp
void ActivateDocObject();
```

### <a name="remarks"></a>Комментарии

`ActivateDocObject` вызывает `IOleDocumentSite` `ActivateMe` метод, но не показывает представление, поскольку он ожидает конкретные инструкции по настройке и отображению представления, заданному в вызове [Кдокобжектсервер:: онактиватевиев](#onactivateview).

Вместе и `ActivateDocObject` `OnActivateView` активизируйте и отобразите представление DocObject. Активация DocObject отличается от других видов активации на месте OLE. DocObject активация обходит отображение границ штриховки на месте и оформлений объектов (таких как маркеры изменения размера), игнорирует функции экстента объектов и рисует полосы прокрутки внутри прямоугольника представления, а не выводит их за пределы этого прямоугольника (как при обычной активации на месте).

## <a name="cdocobjectservercdocobjectserver"></a><a name="cdocobjectserver"></a> Кдокобжектсервер:: Кдокобжектсервер

Создает и инициализирует объект `CDocObjectServer`.

```
explicit CDocObjectServer(
    COleServerDoc* pOwner,
    LPOLEDOCUMENTSITE pDocSite = NULL);
```

### <a name="parameters"></a>Параметры

*повнер*<br/>
Указатель на клиентский документ сайта, который является клиентом для сервера DocObject.

*пдоксите*<br/>
Указатель на интерфейс, `IOleDocumentSite` реализуемый контейнером.

### <a name="remarks"></a>Комментарии

Когда DocObject активен, клиентский интерфейс OLE ( `IOleDocumentSite` ) позволяет серверу DocObject взаимодействовать со своим клиентом (контейнером). Когда сервер DocObject активируется, он сначала проверяет, что контейнер реализует `IOleDocumentSite` интерфейс. Если это так, вызывается [колесервердок:: жетдокобжектсервер](../../mfc/reference/coleserverdoc-class.md#getdocobjectserver) , чтобы проверить, поддерживает ли контейнер докобжектс. По умолчанию `GetDocObjectServer` возвращает значение null. Необходимо переопределить `COleServerDoc::GetDocObjectServer` , чтобы создать новый `CDocObjectServer` объект или производный объект, используя указатели на `COleServerDoc` контейнер и его `IOleDocumentSite` интерфейс в качестве аргументов конструктора.

## <a name="cdocobjectserveronactivateview"></a><a name="onactivateview"></a> Кдокобжектсервер:: Онактиватевиев

Вызовите эту функцию, чтобы отобразить представление DocObject.

```
virtual HRESULT OnActivateView();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение ошибки или предупреждения. По умолчанию в случае успешного выполнения функция возвращает значение "No ERROR". в противном случае E_FAIL.

### <a name="remarks"></a>Комментарии

Эта функция создает окно фрейма на месте, выводит полосы прокрутки в представлении, настраивает меню, которые сервер использует совместно с контейнером, добавляет элементы управления Frame, устанавливает активный объект, затем отображает окно фрейма на месте и устанавливает фокус.

## <a name="cdocobjectserveronapplyviewstate"></a><a name="onapplyviewstate"></a> Кдокобжектсервер:: Онаппливиевстате

Переопределите эту функцию, чтобы восстановить состояние представления DocObject.

```
virtual void OnApplyViewState(CArchive& ar);
```

### <a name="parameters"></a>Параметры

*ar*<br/>
`CArchive`Объект, из которого следует сериализовать состояние представления.

### <a name="remarks"></a>Комментарии

Эта функция вызывается, когда представление отображается в первый раз после его создания. `OnApplyViewState` Инструктирует представление для повторной инициализации в соответствии с данными в `CArchive` объекте, ранее сохраненном с помощью [онсавевиевстате](#onsaveviewstate). Представление должно проверять данные в `CArchive` объекте, так как контейнер не пытается интерпретировать данные состояния представления каким-либо образом.

Можно использовать `OnSaveViewState` для хранения постоянных сведений, относящихся к состоянию представления. При переопределении `OnSaveViewState` для хранения информации необходимо переопределить `OnApplyViewState` для считывания этой информации и применить ее к представлению, когда она вновь активирована.

## <a name="cdocobjectserveronsaveviewstate"></a><a name="onsaveviewstate"></a> Кдокобжектсервер:: Онсавевиевстате

Переопределите эту функцию, чтобы сохранить дополнительные сведения о состоянии представления DocObject.

```
virtual void OnSaveViewState(CArchive& ar);
```

### <a name="parameters"></a>Параметры

*ar*<br/>
`CArchive`Объект, для которого сериализуется состояние представления.

### <a name="remarks"></a>Комментарии

Состояние может включать такие свойства, как тип представления, коэффициент масштабирования, точка вставки и выбора и т. д. Контейнер обычно вызывает эту функцию перед деактивацией представления. Сохраненное состояние можно затем восстановить с помощью [онаппливиевстате](#onapplyviewstate).

Можно использовать `OnSaveViewState` для хранения постоянных сведений, относящихся к состоянию представления. При переопределении `OnSaveViewState` для хранения информации необходимо переопределить `OnApplyViewState` для считывания этой информации и применить ее к представлению, когда она вновь активирована.

## <a name="see-also"></a>См. также раздел

[Класс от CCmdTarget](../../mfc/reference/ccmdtarget-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Кдокобжектсерверитем](../../mfc/reference/cdocobjectserveritem-class.md)
