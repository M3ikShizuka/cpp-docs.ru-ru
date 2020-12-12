---
description: 'Дополнительные сведения о: CD2DTextFormat Class'
title: Класс CD2DTextFormat
ms.date: 03/27/2019
f1_keywords:
- CD2DTextFormat
- AFXRENDERTARGET/CD2DTextFormat
- AFXRENDERTARGET/CD2DTextFormat::CD2DTextFormat
- AFXRENDERTARGET/CD2DTextFormat::Create
- AFXRENDERTARGET/CD2DTextFormat::Destroy
- AFXRENDERTARGET/CD2DTextFormat::Get
- AFXRENDERTARGET/CD2DTextFormat::GetFontFamilyName
- AFXRENDERTARGET/CD2DTextFormat::GetLocaleName
- AFXRENDERTARGET/CD2DTextFormat::IsValid
- AFXRENDERTARGET/CD2DTextFormat::ReCreate
- AFXRENDERTARGET/CD2DTextFormat::m_pTextFormat
helpviewer_keywords:
- CD2DTextFormat [MFC], CD2DTextFormat
- CD2DTextFormat [MFC], Create
- CD2DTextFormat [MFC], Destroy
- CD2DTextFormat [MFC], Get
- CD2DTextFormat [MFC], GetFontFamilyName
- CD2DTextFormat [MFC], GetLocaleName
- CD2DTextFormat [MFC], IsValid
- CD2DTextFormat [MFC], ReCreate
- CD2DTextFormat [MFC], m_pTextFormat
ms.assetid: db194cec-9dae-4644-ab84-7c43b7164117
ms.openlocfilehash: fc87aec6acb0e1eae0211555f1bdc943079081f4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338325"
---
# <a name="cd2dtextformat-class"></a>Класс CD2DTextFormat

Оболочка для Идвритетекстформат.

## <a name="syntax"></a>Синтаксис

```
class CD2DTextFormat : public CD2DResource;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DTextFormat::CD2DTextFormat](#cd2dtextformat)|Конструирует объект CD2DTextFormat.|
|[CD2DTextFormat:: ~ CD2DTextFormat](#_dtorcd2dtextformat)|Деструктор Вызывается при уничтожении объекта формата текста D2D.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CD2DTextFormat:: Create](#create)|Создает CD2DTextFormat. (Переопределяет [CD2DResource:: Create](../../mfc/reference/cd2dresource-class.md#create).)|
|[CD2DTextFormat::D естрой](#destroy)|Уничтожает объект CD2DTextFormat. (Переопределяет [CD2DResource::D естрой](../../mfc/reference/cd2dresource-class.md#destroy).)|
|[CD2DTextFormat:: Get](#get)|Возвращает интерфейс Идвритетекстформат|
|[CD2DTextFormat:: Жетфонтфамилинаме](#getfontfamilyname)|Возвращает копию имени семейства шрифтов.|
|[CD2DTextFormat:: Жетлокаленаме](#getlocalename)|Возвращает копию имени локали.|
|[CD2DTextFormat:: IsValid](#isvalid)|Проверяет допустимость ресурса (переопределяет [CD2DResource:: IsValid](../../mfc/reference/cd2dresource-class.md#isvalid).)|
|[CD2DTextFormat:: повторное создание](#recreate)|Повторно создает CD2DTextFormat. (Переопределяет [CD2DResource:: recreate](../../mfc/reference/cd2dresource-class.md#recreate).)|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CD2DTextFormat:: operator Идвритетекстформат *](#operator_idwritetextformat_star)|Возвращает интерфейс Идвритетекстформат|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CD2DTextFormat:: m_pTextFormat](#m_ptextformat)|Указатель на Идвритетекстформат.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CD2DResource](../../mfc/reference/cd2dresource-class.md)

[CD2DTextFormat](../../mfc/reference/cd2dtextformat-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dtextformatcd2dtextformat"></a><a name="_dtorcd2dtextformat"></a> CD2DTextFormat:: ~ CD2DTextFormat

Деструктор Вызывается при уничтожении объекта формата текста D2D.

```
virtual ~CD2DTextFormat();
```

## <a name="cd2dtextformatcd2dtextformat"></a><a name="cd2dtextformat"></a> CD2DTextFormat::CD2DTextFormat

Конструирует объект CD2DTextFormat.

```
CD2DTextFormat(
    CRenderTarget* pParentTarget,
    const CString& strFontFamilyName,
    FLOAT fontSize,
    DWRITE_FONT_WEIGHT fontWeight = DWRITE_FONT_WEIGHT_NORMAL,
    DWRITE_FONT_STYLE fontStyle = DWRITE_FONT_STYLE_NORMAL,
    DWRITE_FONT_STRETCH fontStretch = DWRITE_FONT_STRETCH_NORMAL,
    const CString& strFontLocale = _T(""),
    IDWriteFontCollection* pFontCollection = NULL,
    BOOL bAutoDestroy = TRUE);
```

### <a name="parameters"></a>Параметры

*ппаренттаржет*<br/>
Указатель на целевой объект прорисовки.

*стрфонтфамилинаме*<br/>
Объект CString, содержащий имя семейства шрифтов.

*fontSize*<br/>
Логический размер шрифта в блоках DIP ("аппаратно-независимые пиксели"). Дипекуалс 1/96 дюйма.

*fontWeight*<br/>
Значение, указывающее насыщенность шрифта для текстового объекта.

*fontStyle*<br/>
Значение, указывающее начертание шрифта для текстового объекта.

*fontStretch*<br/>
Значение, указывающее растяжение шрифта для текстового объекта.

*стрфонтлокале*<br/>
Объект CString, содержащий имя локали.

*пфонтколлектион*<br/>
Указатель на объект коллекции шрифтов. Если это значение равно NULL, указывает на системную коллекцию шрифтов.

*баутодестрой*<br/>
Указывает, что объект будет уничтожен владельцем (Ппаренттаржет).

## <a name="cd2dtextformatcreate"></a><a name="create"></a> CD2DTextFormat:: Create

Создает CD2DTextFormat.

```
virtual HRESULT Create(CRenderTarget* */);
```

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="cd2dtextformatdestroy"></a><a name="destroy"></a> CD2DTextFormat::D естрой

Уничтожает объект CD2DTextFormat.

```
virtual void Destroy();
```

## <a name="cd2dtextformatget"></a><a name="get"></a> CD2DTextFormat:: Get

Возвращает интерфейс Идвритетекстформат

```
IDWriteTextFormat* Get();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс Идвритетекстформат или значение NULL, если объект еще не инициализирован.

## <a name="cd2dtextformatgetfontfamilyname"></a><a name="getfontfamilyname"></a> CD2DTextFormat:: Жетфонтфамилинаме

Возвращает копию имени семейства шрифтов.

```
CString GetFontFamilyName() const;
```

### <a name="return-value"></a>Возвращаемое значение

Объект CString, содержащий имя текущего семейства шрифтов.

## <a name="cd2dtextformatgetlocalename"></a><a name="getlocalename"></a> CD2DTextFormat:: Жетлокаленаме

Возвращает копию имени локали.

```
CString GetLocaleName() const;
```

### <a name="return-value"></a>Возвращаемое значение

Объект CString, содержащий текущее имя языкового стандарта.

## <a name="cd2dtextformatisvalid"></a><a name="isvalid"></a> CD2DTextFormat:: IsValid

Проверка действительности ресурсов

```
virtual BOOL IsValid() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если ресурс является допустимым; в противном случае — FALSE.

## <a name="cd2dtextformatm_ptextformat"></a><a name="m_ptextformat"></a> CD2DTextFormat:: m_pTextFormat

Указатель на Идвритетекстформат.

```
IDWriteTextFormat* m_pTextFormat;
```

## <a name="cd2dtextformatoperator-idwritetextformat"></a><a name="operator_idwritetextformat_star"></a> CD2DTextFormat:: operator Идвритетекстформат *

Возвращает интерфейс Идвритетекстформат

```
operator IDWriteTextFormat*();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс Идвритетекстформат или значение NULL, если объект еще не инициализирован.

## <a name="cd2dtextformatrecreate"></a><a name="recreate"></a> CD2DTextFormat:: повторное создание

Повторно создает CD2DTextFormat.

```
virtual HRESULT ReCreate(CRenderTarget* */);
```

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
