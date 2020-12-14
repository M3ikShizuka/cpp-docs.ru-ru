---
description: 'Дополнительные сведения о: CD2DTextLayout Class'
title: Класс CD2DTextLayout
ms.date: 03/27/2019
f1_keywords:
- CD2DTextLayout
- AFXRENDERTARGET/CD2DTextLayout
- AFXRENDERTARGET/CD2DTextLayout::CD2DTextLayout
- AFXRENDERTARGET/CD2DTextLayout::Create
- AFXRENDERTARGET/CD2DTextLayout::Destroy
- AFXRENDERTARGET/CD2DTextLayout::Get
- AFXRENDERTARGET/CD2DTextLayout::GetFontFamilyName
- AFXRENDERTARGET/CD2DTextLayout::GetLocaleName
- AFXRENDERTARGET/CD2DTextLayout::IsValid
- AFXRENDERTARGET/CD2DTextLayout::ReCreate
- AFXRENDERTARGET/CD2DTextLayout::SetFontFamilyName
- AFXRENDERTARGET/CD2DTextLayout::SetLocaleName
- AFXRENDERTARGET/CD2DTextLayout::m_pTextLayout
helpviewer_keywords:
- CD2DTextLayout [MFC], CD2DTextLayout
- CD2DTextLayout [MFC], Create
- CD2DTextLayout [MFC], Destroy
- CD2DTextLayout [MFC], Get
- CD2DTextLayout [MFC], GetFontFamilyName
- CD2DTextLayout [MFC], GetLocaleName
- CD2DTextLayout [MFC], IsValid
- CD2DTextLayout [MFC], ReCreate
- CD2DTextLayout [MFC], SetFontFamilyName
- CD2DTextLayout [MFC], SetLocaleName
- CD2DTextLayout [MFC], m_pTextLayout
ms.assetid: 724bd13c-f2ef-4e55-a775-8cb04b7b7908
ms.openlocfilehash: 164c8ed5561be6e8f9ee59b07d0aecaced5f7c81
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97240550"
---
# <a name="cd2dtextlayout-class"></a>Класс CD2DTextLayout

Оболочка для Идвритетекстлайаут.

## <a name="syntax"></a>Синтаксис

```
class CD2DTextLayout : public CD2DResource;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DTextLayout::CD2DTextLayout](#cd2dtextlayout)|Конструирует объект CD2DTextLayout.|
|[CD2DTextLayout:: ~ CD2DTextLayout](#_dtorcd2dtextlayout)|Деструктор Вызывается при уничтожении объекта макета текста D2D.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CD2DTextLayout:: Create](#create)|Создает CD2DTextLayout. (Переопределяет [CD2DResource:: Create](../../mfc/reference/cd2dresource-class.md#create).)|
|[CD2DTextLayout::D естрой](#destroy)|Уничтожает объект CD2DTextLayout. (Переопределяет [CD2DResource::D естрой](../../mfc/reference/cd2dresource-class.md#destroy).)|
|[CD2DTextLayout:: Get](#get)|Возвращает интерфейс Идвритетекстлайаут|
|[CD2DTextLayout:: Жетфонтфамилинаме](#getfontfamilyname)|Копирует имя семейства шрифтов для текста в указанной позиции.|
|[CD2DTextLayout:: Жетлокаленаме](#getlocalename)|Возвращает имя локали текста в указанной позиции.|
|[CD2DTextLayout:: IsValid](#isvalid)|Проверяет допустимость ресурса (переопределяет [CD2DResource:: IsValid](../../mfc/reference/cd2dresource-class.md#isvalid).)|
|[CD2DTextLayout:: повторное создание](#recreate)|Повторно создает CD2DTextLayout. (Переопределяет [CD2DResource:: recreate](../../mfc/reference/cd2dresource-class.md#recreate).)|
|[CD2DTextLayout:: Сетфонтфамилинаме](#setfontfamilyname)|Задает имя семейства шрифтов, заканчивающееся нулем, для текста в указанном текстовом диапазоне|
|[CD2DTextLayout:: Сетлокаленаме](#setlocalename)|Задает имя локали для текста в указанном текстовом диапазоне|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CD2DTextLayout:: operator Идвритетекстлайаут *](#operator_idwritetextlayout_star)|Возвращает интерфейс Идвритетекстлайаут|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CD2DTextLayout:: m_pTextLayout](#m_ptextlayout)|Указатель на Идвритетекстлайаут.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CD2DResource](../../mfc/reference/cd2dresource-class.md)

[CD2DTextLayout](../../mfc/reference/cd2dtextlayout-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dtextlayoutcd2dtextlayout"></a><a name="_dtorcd2dtextlayout"></a> CD2DTextLayout:: ~ CD2DTextLayout

Деструктор Вызывается при уничтожении объекта макета текста D2D.

```
virtual ~CD2DTextLayout();
```

## <a name="cd2dtextlayoutcd2dtextlayout"></a><a name="cd2dtextlayout"></a> CD2DTextLayout::CD2DTextLayout

Конструирует объект CD2DTextLayout.

```
CD2DTextLayout(
    CRenderTarget* pParentTarget,
    const CString& strText,
    CD2DTextFormat& textFormat,
    const CD2DSizeF& sizeMax,
    BOOL bAutoDestroy = TRUE);
```

### <a name="parameters"></a>Параметры

*ппаренттаржет*<br/>
Указатель на целевой объект прорисовки.

*стртекст*<br/>
Объект CString, содержащий строку для создания нового объекта CD2DTextLayout из.

*textFormat*<br/>
Объект CString, содержащий формат, применяемый к строке.

*сиземакс*<br/>
Размер поля макета.

*баутодестрой*<br/>
Указывает, что объект будет уничтожен владельцем (Ппаренттаржет).

## <a name="cd2dtextlayoutcreate"></a><a name="create"></a> CD2DTextLayout:: Create

Создает CD2DTextLayout.

```
virtual HRESULT Create(CRenderTarget* */);
```

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="cd2dtextlayoutdestroy"></a><a name="destroy"></a> CD2DTextLayout::D естрой

Уничтожает объект CD2DTextLayout.

```
virtual void Destroy();
```

## <a name="cd2dtextlayoutget"></a><a name="get"></a> CD2DTextLayout:: Get

Возвращает интерфейс Идвритетекстлайаут

```
IDWriteTextLayout* Get();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс Идвритетекстлайаут или значение NULL, если объект еще не инициализирован.

## <a name="cd2dtextlayoutgetfontfamilyname"></a><a name="getfontfamilyname"></a> CD2DTextLayout:: Жетфонтфамилинаме

Копирует имя семейства шрифтов для текста в указанной позиции.

```
CString GetFontFamilyName(
    UINT32 currentPosition,
    DWRITE_TEXT_RANGE* textRange = NULL) const;
```

### <a name="parameters"></a>Параметры

*currentPosition*<br/>
Расположение текста для проверки.

*textRange*<br/>
Диапазон текста с тем же форматированием, что и у текста в позиции, заданной параметром currentPosition. Это означает, что выполнение имеет точное форматирование в соответствии с указанной позицией, включая, но не ограниченное именем семейства шрифтов.

### <a name="return-value"></a>Возвращаемое значение

Объект CString, содержащий имя текущего семейства шрифтов.

## <a name="cd2dtextlayoutgetlocalename"></a><a name="getlocalename"></a> CD2DTextLayout:: Жетлокаленаме

Возвращает имя локали текста в указанной позиции.

```
CString GetLocaleName(
    UINT32 currentPosition,
    DWRITE_TEXT_RANGE* textRange = NULL) const;
```

### <a name="parameters"></a>Параметры

*currentPosition*<br/>
Расположение текста для проверки.

*textRange*<br/>
Диапазон текста с тем же форматированием, что и у текста в позиции, заданной параметром currentPosition. Это означает, что выполнение имеет точное форматирование в соответствии с заданной позицией, включая, но не ограниченное названием языкового стандарта.

### <a name="return-value"></a>Возвращаемое значение

Объект CString, содержащий текущее имя языкового стандарта.

## <a name="cd2dtextlayoutisvalid"></a><a name="isvalid"></a> CD2DTextLayout:: IsValid

Проверка действительности ресурсов

```
virtual BOOL IsValid() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если ресурс является допустимым; в противном случае — FALSE.

## <a name="cd2dtextlayoutm_ptextlayout"></a><a name="m_ptextlayout"></a> CD2DTextLayout:: m_pTextLayout

Указатель на Идвритетекстлайаут.

```
IDWriteTextLayout* m_pTextLayout;
```

## <a name="cd2dtextlayoutoperator-idwritetextlayout"></a><a name="operator_idwritetextlayout_star"></a> CD2DTextLayout:: operator Идвритетекстлайаут *

Возвращает интерфейс Идвритетекстлайаут

```
operator IDWriteTextLayout*();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс Идвритетекстлайаут или значение NULL, если объект еще не инициализирован.

## <a name="cd2dtextlayoutrecreate"></a><a name="recreate"></a> CD2DTextLayout:: повторное создание

Повторно создает CD2DTextLayout.

```
virtual HRESULT ReCreate(CRenderTarget* */);
```

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="cd2dtextlayoutsetfontfamilyname"></a><a name="setfontfamilyname"></a> CD2DTextLayout:: Сетфонтфамилинаме

Задает имя семейства шрифтов, заканчивающееся нулем, для текста в указанном текстовом диапазоне

```
BOOL SetFontFamilyName(
    LPCWSTR pwzFontFamilyName,
    DWRITE_TEXT_RANGE textRange);
```

### <a name="parameters"></a>Параметры

*пвзфонтфамилинаме*<br/>
Имя семейства шрифтов, которое применяется ко всей текстовой строке в диапазоне, заданном аргументом textRange

*textRange*<br/>
Диапазон текста, к которому применяется это изменение

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="cd2dtextlayoutsetlocalename"></a><a name="setlocalename"></a> CD2DTextLayout:: Сетлокаленаме

Задает имя локали для текста в указанном текстовом диапазоне

```
BOOL SetLocaleName(
    LPCWSTR pwzLocaleName,
    DWRITE_TEXT_RANGE textRange);
```

### <a name="parameters"></a>Параметры

*пвзлокаленаме*<br/>
Строка имени локали, заканчивающаяся нулем

*textRange*<br/>
Диапазон текста, к которому применяется это изменение

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
