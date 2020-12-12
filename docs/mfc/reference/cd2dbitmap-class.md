---
description: 'Дополнительные сведения о: CD2DBitmap Class'
title: Класс CD2DBitmap
ms.date: 11/04/2016
f1_keywords:
- CD2DBitmap
- AFXRENDERTARGET/CD2DBitmap
- AFXRENDERTARGET/CD2DBitmap::CD2DBitmap
- AFXRENDERTARGET/CD2DBitmap::Attach
- AFXRENDERTARGET/CD2DBitmap::CopyFromBitmap
- AFXRENDERTARGET/CD2DBitmap::CopyFromMemory
- AFXRENDERTARGET/CD2DBitmap::CopyFromRenderTarget
- AFXRENDERTARGET/CD2DBitmap::Create
- AFXRENDERTARGET/CD2DBitmap::Destroy
- AFXRENDERTARGET/CD2DBitmap::Detach
- AFXRENDERTARGET/CD2DBitmap::Get
- AFXRENDERTARGET/CD2DBitmap::GetDPI
- AFXRENDERTARGET/CD2DBitmap::GetPixelFormat
- AFXRENDERTARGET/CD2DBitmap::GetPixelSize
- AFXRENDERTARGET/CD2DBitmap::GetSize
- AFXRENDERTARGET/CD2DBitmap::IsValid
- AFXRENDERTARGET/CD2DBitmap::CommonInit
- AFXRENDERTARGET/CD2DBitmap::m_bAutoDestroyHBMP
- AFXRENDERTARGET/CD2DBitmap::m_hBmpSrc
- AFXRENDERTARGET/CD2DBitmap::m_lpszType
- AFXRENDERTARGET/CD2DBitmap::m_pBitmap
- AFXRENDERTARGET/CD2DBitmap::m_sizeDest
- AFXRENDERTARGET/CD2DBitmap::m_strPath
- AFXRENDERTARGET/CD2DBitmap::m_uiResID
helpviewer_keywords:
- CD2DBitmap [MFC], CD2DBitmap
- CD2DBitmap [MFC], CD2DBitmap
- CD2DBitmap [MFC], Attach
- CD2DBitmap [MFC], CopyFromBitmap
- CD2DBitmap [MFC], CopyFromMemory
- CD2DBitmap [MFC], CopyFromRenderTarget
- CD2DBitmap [MFC], Create
- CD2DBitmap [MFC], Destroy
- CD2DBitmap [MFC], Detach
- CD2DBitmap [MFC], Get
- CD2DBitmap [MFC], GetDPI
- CD2DBitmap [MFC], GetPixelFormat
- CD2DBitmap [MFC], GetPixelSize
- CD2DBitmap [MFC], GetSize
- CD2DBitmap [MFC], IsValid
- CD2DBitmap [MFC], CommonInit
- CD2DBitmap [MFC], m_bAutoDestroyHBMP
- CD2DBitmap [MFC], m_hBmpSrc
- CD2DBitmap [MFC], m_lpszType
- CD2DBitmap [MFC], m_pBitmap
- CD2DBitmap [MFC], m_sizeDest
- CD2DBitmap [MFC], m_strPath
- CD2DBitmap [MFC], m_uiResID
ms.assetid: 2b3686f1-812c-462b-b449-9f0cb6949bf6
ms.openlocfilehash: ab023caa92683b24098db1a03d081922e3dfd48b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97227654"
---
# <a name="cd2dbitmap-class"></a>Класс CD2DBitmap

Оболочка для ID2D1Bitmap.

## <a name="syntax"></a>Синтаксис

```
class CD2DBitmap : public CD2DResource;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DBitmap::CD2DBitmap](#cd2dbitmap)|Перегружен. Конструирует объект CD2DBitmap из ХБИТМАП.|
|[CD2DBitmap:: ~ CD2DBitmap](#_dtorcd2dbitmap)|Деструктор Вызывается при уничтожении объекта Bitmap D2D.|

### <a name="protected-constructors"></a>Защищенные конструкторы

|Имя|Описание|
|----------|-----------------|
|[CD2DBitmap::CD2DBitmap](#cd2dbitmap)|Перегружен. Конструирует объект CD2DBitmap.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CD2DBitmap:: Attach](#attach)|Присоединяет существующий интерфейс ресурсов к объекту|
|[CD2DBitmap:: Копифромбитмап](#copyfrombitmap)|Копирует указанную область из указанного растрового изображения в текущее растровое изображение|
|[CD2DBitmap:: Копифроммемори](#copyfrommemory)|Копирует указанный регион из памяти в текущее растровое изображение|
|[CD2DBitmap:: Копифромрендертаржет](#copyfromrendertarget)|Копирует указанный регион из указанного целевого объекта отрисовки в текущее растровое изображение|
|[CD2DBitmap:: Create](#create)|Создает CD2DBitmap. (Переопределяет [CD2DResource:: Create](../../mfc/reference/cd2dresource-class.md#create).)|
|[CD2DBitmap::D естрой](#destroy)|Уничтожает объект CD2DBitmap. (Переопределяет [CD2DResource::D естрой](../../mfc/reference/cd2dresource-class.md#destroy).)|
|[CD2DBitmap::D етач](#detach)|Отсоединяет интерфейс ресурса от объекта|
|[CD2DBitmap:: Get](#get)|Возвращает интерфейс ID2D1Bitmap|
|[CD2DBitmap:: GetDPI](#getdpi)|Возврат точек на дюйм точечного рисунка (DPI)|
|[CD2DBitmap:: Жетпикселформат](#getpixelformat)|Получает формат пикселей и альфа-режим точечного рисунка|
|[CD2DBitmap:: Жетпикселсизе](#getpixelsize)|Возвращает размер точечного рисунка (в пикселях), зависящих от устройства (ПКС)|
|[CD2DBitmap:: DataSize](#getsize)|Возвращает размер точечного рисунка в пикселях, не зависящих от устройства (DIP).|
|[CD2DBitmap:: IsValid](#isvalid)|Проверяет допустимость ресурса (переопределяет [CD2DResource:: IsValid](../../mfc/reference/cd2dresource-class.md#isvalid).)|

### <a name="protected-methods"></a>Защищенные методы

|Имя|Описание|
|----------|-----------------|
|[CD2DBitmap:: Коммонинит](#commoninit)|Инициализирует объект|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CD2DBitmap:: operator ID2D1Bitmap *](#operator_id2d1bitmap_star)|Возвращает интерфейс ID2D1Bitmap|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CD2DBitmap:: m_bAutoDestroyHBMP](#m_bautodestroyhbmp)|Значение TRUE, если m_hBmpSrc следует уничтожить; в противном случае — FALSE.|
|[CD2DBitmap:: m_hBmpSrc](#m_hbmpsrc)|Маркер исходного растрового изображения.|
|[CD2DBitmap:: m_lpszType](#m_lpsztype)|Тип ресурса.|
|[CD2DBitmap:: m_pBitmap](#m_pbitmap)|Хранит указатель на объект ID2D1Bitmap.|
|[CD2DBitmap:: m_sizeDest](#m_sizedest)|Размер назначения точечного рисунка.|
|[CD2DBitmap:: m_strPath](#m_strpath)|Путь к файлу ботмап.|
|[CD2DBitmap:: m_uiResID](#m_uiresid)|Идентификатор ресурса точечного рисунка.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CD2DResource](../../mfc/reference/cd2dresource-class.md)

`CD2DBitmap`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dbitmapcd2dbitmap"></a><a name="_dtorcd2dbitmap"></a> CD2DBitmap:: ~ CD2DBitmap

Деструктор Вызывается при уничтожении объекта Bitmap D2D.

```
virtual ~CD2DBitmap();
```

## <a name="cd2dbitmapattach"></a><a name="attach"></a> CD2DBitmap:: Attach

Присоединяет существующий интерфейс ресурсов к объекту.

```cpp
void Attach(ID2D1Bitmap* pResource);
```

### <a name="parameters"></a>Параметры

*исходный код*<br/>
Существующий интерфейс ресурсов. Не может быть NULL.

## <a name="cd2dbitmapcd2dbitmap"></a><a name="cd2dbitmap"></a> CD2DBitmap::CD2DBitmap

Конструирует объект CD2DBitmap из ресурса.

```
CD2DBitmap(
    CRenderTarget* pParentTarget,
    UINT uiResID,
    LPCTSTR lpszType = NULL,
    CD2DSizeU sizeDest = CD2DSizeU(0, 0),
    BOOL bAutoDestroy = TRUE);

CD2DBitmap(
    CRenderTarget* pParentTarget,
    LPCTSTR lpszPath,
    CD2DSizeU sizeDest = CD2DSizeU(0, 0),
    BOOL bAutoDestroy = TRUE);

CD2DBitmap(
    CRenderTarget* pParentTarget,
    HBITMAP hbmpSrc,
    CD2DSizeU sizeDest = CD2DSizeU(0, 0),
    BOOL bAutoDestroy = TRUE);

CD2DBitmap(
    CRenderTarget* pParentTarget,
    BOOL bAutoDestroy = TRUE);
```

### <a name="parameters"></a>Параметры

*ппаренттаржет*<br/>
Указатель на целевой объект прорисовки.

*уиресид*<br/>
ИДЕНТИФИКАЦИОНный номер ресурса.

*лпсзтипе*<br/>
Указатель на строку, завершающуюся нулем, которая содержит тип ресурса.

*самый заданный размер*<br/>
Целевой размер точечного рисунка.

*баутодестрой*<br/>
Указывает, что объект будет уничтожен владельцем (Ппаренттаржет).

*лпсзпас*<br/>
Указатель на строку, завершающуюся нулем, которая содержит имя файла.

*хбмпсрк*<br/>
Маркер для точечного рисунка.

## <a name="cd2dbitmapcommoninit"></a><a name="commoninit"></a> CD2DBitmap:: Коммонинит

Инициализирует объект.

```cpp
void CommonInit();
```

## <a name="cd2dbitmapcopyfrombitmap"></a><a name="copyfrombitmap"></a> CD2DBitmap:: Копифромбитмап

Копирует указанную область из указанного растрового изображения в текущее растровое изображение.

```
HRESULT CopyFromBitmap(
    const CD2DBitmap* pBitmap,
    const CD2DPointU* destPoint = NULL,
    const CD2DRectU* srcRect = NULL);
```

### <a name="parameters"></a>Параметры

*пбитмап*<br/>
Битовая карта, из которой производится копирование.

*дестпоинт*<br/>
В текущем битовом рисунке верхний левый угол области, в которую копируется регион, заданный параметром srcRect.

*srcRect*<br/>
Область копируемого растрового изображения.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="cd2dbitmapcopyfrommemory"></a><a name="copyfrommemory"></a> CD2DBitmap:: Копифроммемори

Копирует указанный регион из памяти в текущее растровое изображение.

```
HRESULT CopyFromMemory(
    const void* srcData,
    UINT32 pitch,
    const CD2DRectU* destRect = NULL);
```

### <a name="parameters"></a>Параметры

*srcData*<br/>
Копируемые данные.

*тон*<br/>
Шаг или шаг исходного растрового изображения, хранящегося в srcData. Шаг — это число байтов сканлине (одна строка пикселей в памяти). Шаг можно вычислить по следующей формуле: ширина пикселей \* в байтах на пиксель и заполнение памяти.

*дестрект*<br/>
В текущем битовом рисунке верхний левый угол области, в которую копируется регион, заданный параметром srcRect.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="cd2dbitmapcopyfromrendertarget"></a><a name="copyfromrendertarget"></a> CD2DBitmap:: Копифромрендертаржет

Копирует указанный регион из указанного целевого объекта отрисовки в текущее растровое изображение.

```
HRESULT CopyFromRenderTarget(
    const CRenderTarget* pRenderTarget,
    const CD2DPointU* destPoint = NULL,
    const CD2DRectU* srcRect = NULL);
```

### <a name="parameters"></a>Параметры

*прендертаржет*<br/>
Целевой объект отрисовки, содержащий копируемый регион.

*дестпоинт*<br/>
В текущем битовом рисунке верхний левый угол области, в которую копируется регион, заданный параметром srcRect.

*srcRect*<br/>
Область Рендертаржет для копирования.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="cd2dbitmapcreate"></a><a name="create"></a> CD2DBitmap:: Create

Создает CD2DBitmap.

```
virtual HRESULT Create(CRenderTarget* pRenderTarget);
```

### <a name="parameters"></a>Параметры

*прендертаржет*<br/>
Указатель на целевой объект прорисовки.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="cd2dbitmapdestroy"></a><a name="destroy"></a> CD2DBitmap::D естрой

Уничтожает объект CD2DBitmap.

```
virtual void Destroy();
```

## <a name="cd2dbitmapdetach"></a><a name="detach"></a> CD2DBitmap::D етач

Отсоединяет интерфейс ресурса от объекта.

```
ID2D1Bitmap* Detach();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на отсоединенный интерфейс ресурсов.

## <a name="cd2dbitmapget"></a><a name="get"></a> CD2DBitmap:: Get

Возвращает интерфейс ID2D1Bitmap.

```
ID2D1Bitmap* Get();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1Bitmap или значение NULL, если объект еще не инициализирован.

## <a name="cd2dbitmapgetdpi"></a><a name="getdpi"></a> CD2DBitmap:: GetDPI

Возврат точек на дюйм точечного рисунка (DPI).

```
CD2DSizeF GetDPI() const;
```

### <a name="return-value"></a>Возвращаемое значение

Горизонтальное и вертикальное разрешение точечного рисунка.

## <a name="cd2dbitmapgetpixelformat"></a><a name="getpixelformat"></a> CD2DBitmap:: Жетпикселформат

Получает формат пикселей и альфа-режим точечного рисунка

```
D2D1_PIXEL_FORMAT GetPixelFormat() const;
```

### <a name="return-value"></a>Возвращаемое значение

Формат пикселей и альфа-режим точечного рисунка.

## <a name="cd2dbitmapgetpixelsize"></a><a name="getpixelsize"></a> CD2DBitmap:: Жетпикселсизе

Возвращает размер точечного рисунка в единицах измерения, зависящих от устройства (в пикселях).

```
CD2DSizeU GetPixelSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Размер точечного рисунка (в пикселях).

## <a name="cd2dbitmapgetsize"></a><a name="getsize"></a> CD2DBitmap:: DataSize

Возвращает размер точечного рисунка в пикселях, не зависящих от устройства (DIP).

```
CD2DSizeF GetSize() const;
```

### <a name="return-value"></a>Возвращаемое значение

Размер точечного рисунка в DIP.

## <a name="cd2dbitmapisvalid"></a><a name="isvalid"></a> CD2DBitmap:: IsValid

Проверяет допустимость ресурсов.

```
virtual BOOL IsValid() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если ресурс является допустимым; в противном случае — FALSE.

## <a name="cd2dbitmapm_bautodestroyhbmp"></a><a name="m_bautodestroyhbmp"></a> CD2DBitmap:: m_bAutoDestroyHBMP

Значение TRUE, если m_hBmpSrc следует уничтожить; в противном случае — FALSE.

```
BOOL m_bAutoDestroyHBMP;
```

## <a name="cd2dbitmapm_hbmpsrc"></a><a name="m_hbmpsrc"></a> CD2DBitmap:: m_hBmpSrc

Маркер исходного растрового изображения.

```
HBITMAP m_hBmpSrc;
```

## <a name="cd2dbitmapm_lpsztype"></a><a name="m_lpsztype"></a> CD2DBitmap:: m_lpszType

Тип ресурса.

```
LPCTSTR m_lpszType;
```

## <a name="cd2dbitmapm_pbitmap"></a><a name="m_pbitmap"></a> CD2DBitmap:: m_pBitmap

Хранит указатель на объект ID2D1Bitmap.

```
ID2D1Bitmap* m_pBitmap;
```

## <a name="cd2dbitmapm_sizedest"></a><a name="m_sizedest"></a> CD2DBitmap:: m_sizeDest

Размер назначения точечного рисунка.

```
CD2DSizeU m_sizeDest;
```

## <a name="cd2dbitmapm_strpath"></a><a name="m_strpath"></a> CD2DBitmap:: m_strPath

Путь к файлу ботмап.

```
CString m_strPath;
```

## <a name="cd2dbitmapm_uiresid"></a><a name="m_uiresid"></a> CD2DBitmap:: m_uiResID

Идентификатор ресурса точечного рисунка.

```
UINT m_uiResID;
```

## <a name="cd2dbitmapoperator-id2d1bitmap"></a><a name="operator_id2d1bitmap_star"></a> CD2DBitmap:: operator ID2D1Bitmap *

Возвращает интерфейс ID2D1Bitmap

```
operator ID2D1Bitmap*();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1Bitmap или значение NULL, если объект еще не инициализирован.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
