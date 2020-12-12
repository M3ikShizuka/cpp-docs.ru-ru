---
description: 'Дополнительные сведения о: CPictureHolder Class'
title: Класс CPictureHolder
ms.date: 11/04/2016
f1_keywords:
- CPictureHolder
- AFXCTL/CPictureHolder
- AFXCTL/CPictureHolder::CPictureHolder
- AFXCTL/CPictureHolder::CreateEmpty
- AFXCTL/CPictureHolder::CreateFromBitmap
- AFXCTL/CPictureHolder::CreateFromIcon
- AFXCTL/CPictureHolder::CreateFromMetafile
- AFXCTL/CPictureHolder::GetDisplayString
- AFXCTL/CPictureHolder::GetPictureDispatch
- AFXCTL/CPictureHolder::GetType
- AFXCTL/CPictureHolder::Render
- AFXCTL/CPictureHolder::SetPictureDispatch
- AFXCTL/CPictureHolder::m_pPict
helpviewer_keywords:
- CPictureHolder [MFC], CPictureHolder
- CPictureHolder [MFC], CreateEmpty
- CPictureHolder [MFC], CreateFromBitmap
- CPictureHolder [MFC], CreateFromIcon
- CPictureHolder [MFC], CreateFromMetafile
- CPictureHolder [MFC], GetDisplayString
- CPictureHolder [MFC], GetPictureDispatch
- CPictureHolder [MFC], GetType
- CPictureHolder [MFC], Render
- CPictureHolder [MFC], SetPictureDispatch
- CPictureHolder [MFC], m_pPict
ms.assetid: a4f59775-704a-41dd-b5bd-2e531c95127a
ms.openlocfilehash: 47eacb66191e21b300aaa0d06bc23155fabaf651
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97301481"
---
# <a name="cpictureholder-class"></a>Класс CPictureHolder

Реализует свойство изображения, которое позволяет пользователю отображать изображение в элементе управления.

## <a name="syntax"></a>Синтаксис

```
class CPictureHolder
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CPictureHolder:: CPictureHolder](#cpictureholder)|Формирует объект `CPictureHolder`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CPictureHolder:: Креатимпти](#createempty)|Создает пустой объект `CPictureHolder`.|
|[CPictureHolder:: Креатефромбитмап](#createfrombitmap)|Создает `CPictureHolder` объект из точечного рисунка.|
|[CPictureHolder:: Креатефромикон](#createfromicon)|Создает `CPictureHolder` объект из значка.|
|[CPictureHolder:: Креатефромметафиле](#createfrommetafile)|Создает `CPictureHolder` объект из метафайла.|
|[CPictureHolder:: Жетдисплайстринг](#getdisplaystring)|Извлекает строку, отображаемую в обозревателе свойств контейнера элемента управления.|
|[CPictureHolder:: Жетпиктуредиспатч](#getpicturedispatch)|Возвращает `CPictureHolder` `IDispatch` интерфейс объекта.|
|[CPictureHolder:: GetType](#gettype)|Указывает `CPictureHolder` , является ли объект точечным рисунком, метафайлом или значком.|
|[CPictureHolder:: Render](#render)|Визуализирует изображение.|
|[CPictureHolder:: Сетпиктуредиспатч](#setpicturedispatch)|Задает `CPictureHolder` `IDispatch` интерфейс объекта.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[CPictureHolder:: m_pPict](#m_ppict)|Указатель на объект изображения.|

## <a name="remarks"></a>Комментарии

`CPictureHolder` не имеет базового класса.

С помощью свойства «изображение акции» разработчик может указать точечный рисунок, значок или метафайл для вывода.

Сведения о создании настраиваемых свойств рисунка см. в статье [элементы управления ActiveX в MFC. Использование рисунков в элементе управления ActiveX](../../mfc/mfc-activex-controls-using-pictures-in-an-activex-control.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CPictureHolder`

## <a name="requirements"></a>Требования

**Заголовок:** afxctl. h

## <a name="cpictureholdercpictureholder"></a><a name="cpictureholder"></a> CPictureHolder:: CPictureHolder

Формирует объект `CPictureHolder`.

```
CPictureHolder();
```

## <a name="cpictureholdercreateempty"></a><a name="createempty"></a> CPictureHolder:: Креатимпти

Создает пустой `CPictureHolder` объект и подключает его к `IPicture` интерфейсу.

```
BOOL CreateEmpty();
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если объект успешно создан; в противном случае — 0.

## <a name="cpictureholdercreatefrombitmap"></a><a name="createfrombitmap"></a> CPictureHolder:: Креатефромбитмап

Использует точечный рисунок для инициализации объекта изображения в `CPictureHolder` .

```
BOOL CreateFromBitmap(
    UINT idResource);

BOOL CreateFromBitmap(
    CBitmap* pBitmap,
    CPalette* pPal = NULL,
    BOOL bTransferOwnership = TRUE);

BOOL CreateFromBitmap(
    HBITMAP hbm,
    HPALETTE hpal = NULL,
    BOOL bTransferOwnership = FALSE);
```

### <a name="parameters"></a>Параметры

*идресаурце*<br/>
Идентификатор ресурса точечного рисунка.

*пбитмап*<br/>
Указатель на объект [CBitmap](../../mfc/reference/cbitmap-class.md) .

*ппал*<br/>
Указатель на объект [кпалетте](../../mfc/reference/cpalette-class.md) .

*бтрансферовнершип*<br/>
Указывает, будет ли объект изображения становиться владельцем объектов Bitmap и Palette.

*хбм*<br/>
Обработчик для растрового изображения, из которого `CPictureHolder` создается объект.

*хпал*<br/>
Обработка палитры, используемой для отрисовки точечного рисунка.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если объект успешно создан; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Если *бтрансферовнершип* имеет значение true, вызывающий объект не должен использовать растровое изображение или объекты палитры каким-либо образом после возврата этого вызова. Если *бтрансферовнершип* имеет значение false, вызывающий объект отвечает за обеспечение допустимости объектов Bitmap и Palette в течение времени существования объекта изображения.

## <a name="cpictureholdercreatefromicon"></a><a name="createfromicon"></a> CPictureHolder:: Креатефромикон

Использует значок для инициализации объекта изображения в `CPictureHolder` .

```
BOOL CreateFromIcon(
    UINT idResource);

BOOL CreateFromIcon(
    HICON hIcon,
    BOOL bTransferOwnership = FALSE);
```

### <a name="parameters"></a>Параметры

*идресаурце*<br/>
Идентификатор ресурса точечного рисунка.

*hIcon*<br/>
Обработчик для значка, из которого `CPictureHolder` создается объект.

*бтрансферовнершип*<br/>
Указывает, будет ли объект изображения становиться владельцем объекта значка.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если объект успешно создан; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Если *бтрансферовнершип* имеет значение true, вызывающая сторона не должна использовать объект Icon каким-либо образом после возврата этого вызова. Если *бтрансферовнершип* имеет значение false, то вызывающая сторона несет ответственность за обеспечение того, что объект значка остается действительным в течение времени существования объекта изображения.

## <a name="cpictureholdercreatefrommetafile"></a><a name="createfrommetafile"></a> CPictureHolder:: Креатефромметафиле

Использует метафайл для инициализации объекта изображения в `CPictureHolder` .

```
BOOL CreateFromMetafile(
    HMETAFILE hmf,
    int xExt,
    int yExt,
    BOOL bTransferOwnership = FALSE);
```

### <a name="parameters"></a>Параметры

*хмф*<br/>
Маркер для метафайла, используемого для создания `CPictureHolder` объекта.

*ксекст*<br/>
Экстент изображения на X.

*екст*<br/>
Область Y изображения.

*бтрансферовнершип*<br/>
Указывает, будет ли объект изображения становиться владельцем объекта Metafile.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если объект успешно создан; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Если *бтрансферовнершип* имеет значение true, то вызывающая сторона не должна использовать объект Metafile каким-либо образом после возврата этого вызова. Если *бтрансферовнершип* имеет значение false, вызывающий объект отвечает за обеспечение допустимости объекта Metafile в течение времени существования объекта изображения.

## <a name="cpictureholdergetdisplaystring"></a><a name="getdisplaystring"></a> CPictureHolder:: Жетдисплайстринг

Извлекает строку, отображаемую в обозревателе свойств контейнера.

```
BOOL GetDisplayString(CString& strValue);
```

### <a name="parameters"></a>Параметры

*strValue*<br/>
Ссылка на [CString](../../atl-mfc-shared/reference/cstringt-class.md) , который будет содержать отображаемую строку.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если строка успешно получена; в противном случае — 0.

## <a name="cpictureholdergetpicturedispatch"></a><a name="getpicturedispatch"></a> CPictureHolder:: Жетпиктуредиспатч

Эта функция возвращает указатель на `CPictureHolder` `IPictureDisp` интерфейс объекта.

```
LPPICTUREDISP GetPictureDispatch();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на `CPictureHolder` `IPictureDisp` интерфейс объекта.

### <a name="remarks"></a>Комментарии

Вызывающий объект должен вызвать `Release` по этому указателю, когда он завершится с ним.

## <a name="cpictureholdergettype"></a><a name="gettype"></a> CPictureHolder:: GetType

Указывает, является ли изображение точечным рисунком, метафайлом или значком.

```
short GetType();
```

### <a name="return-value"></a>Возвращаемое значение

Значение типа, указывающее тип изображения. Возможны следующие значения и их значение.

|Значение|Значение|
|-----------|-------------|
|PICTYPE_UNINITIALIZED|`CPictureHolder` Объект — унититиализед.|
|PICTYPE_NONE|`CPictureHolder` Объект пуст.|
|PICTYPE_BITMAP|Рисунок является точечным рисунком.|
|PICTYPE_METAFILE|Рисунок является метафайлом.|
|PICTYPE_ICON|Изображение является значком.|

## <a name="cpictureholderm_ppict"></a><a name="m_ppict"></a> CPictureHolder:: m_pPict

Указатель на `CPictureHolder` `IPicture` интерфейс объекта.

```
LPPICTURE m_pPict;
```

## <a name="cpictureholderrender"></a><a name="render"></a> CPictureHolder:: Render

Визуализирует изображение в прямоугольнике, на который ссылается *ркрендер*.

```cpp
void Render(
    CDC* pDC,
    const CRect& rcRender,
    const CRect& rcWBounds);
```

### <a name="parameters"></a>Параметры

*Хозяин*<br/>
Указатель на контекст отображения, в котором будет отображаться изображение.

*ркрендер*<br/>
Прямоугольник, в котором будет отображаться изображение.

*рквбаундс*<br/>
Прямоугольник, представляющий ограничивающий прямоугольник объекта, который подготовит к просмотру изображение. Для элемента управления этот прямоугольник является параметром *ркбаундс* , передаваемым переопределению [COleControl:: OnDraw](../../mfc/reference/colecontrol-class.md#ondraw).

## <a name="cpictureholdersetpicturedispatch"></a><a name="setpicturedispatch"></a> CPictureHolder:: Сетпиктуредиспатч

Подключает `CPictureHolder` объект к `IPictureDisp` интерфейсу.

```cpp
void SetPictureDispatch(LPPICTUREDISP pDisp);
```

### <a name="parameters"></a>Параметры

*пдисп*<br/>
Указатель на новый `IPictureDisp` интерфейс.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Кфонсолдер](../../mfc/reference/cfontholder-class.md)
