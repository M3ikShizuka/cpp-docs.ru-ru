---
description: 'Дополнительные сведения о: Ккэйфраме Class'
title: Класс CKeyFrame
ms.date: 11/04/2016
f1_keywords:
- CKeyFrame
- AFXANIMATIONCONTROLLER/CKeyFrame
- AFXANIMATIONCONTROLLER/CKeyFrame::CKeyFrame
- AFXANIMATIONCONTROLLER/CKeyFrame::AddToStoryboard
- AFXANIMATIONCONTROLLER/CKeyFrame::AddToStoryboardAfterTransition
- AFXANIMATIONCONTROLLER/CKeyFrame::AddToStoryboardAtOffset
- AFXANIMATIONCONTROLLER/CKeyFrame::GetExistingKeyframe
- AFXANIMATIONCONTROLLER/CKeyFrame::GetOffset
- AFXANIMATIONCONTROLLER/CKeyFrame::GetTransition
- AFXANIMATIONCONTROLLER/CKeyFrame::m_offset
- AFXANIMATIONCONTROLLER/CKeyFrame::m_pExistingKeyFrame
- AFXANIMATIONCONTROLLER/CKeyFrame::m_pTransition
helpviewer_keywords:
- CKeyFrame [MFC], CKeyFrame
- CKeyFrame [MFC], AddToStoryboard
- CKeyFrame [MFC], AddToStoryboardAfterTransition
- CKeyFrame [MFC], AddToStoryboardAtOffset
- CKeyFrame [MFC], GetExistingKeyframe
- CKeyFrame [MFC], GetOffset
- CKeyFrame [MFC], GetTransition
- CKeyFrame [MFC], m_offset
- CKeyFrame [MFC], m_pExistingKeyFrame
- CKeyFrame [MFC], m_pTransition
ms.assetid: d050a562-20f6-4c65-8ce5-ccb3aef1a20e
ms.openlocfilehash: ec6aa45484965afbf0c636a1eed26a3d4a63e426
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97236884"
---
# <a name="ckeyframe-class"></a>Класс CKeyFrame

Представляет ключевой кадр анимации.

## <a name="syntax"></a>Синтаксис

```
class CKeyFrame : public CBaseKeyFrame;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккэйфраме:: Ккэйфраме](#ckeyframe)|Перегружен. Конструирует опорный кадр, зависящий от другого опорного кадра.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккэйфраме:: Аддтосторибоард](#addtostoryboard)|Добавляет опорный кадр в раскадровку. (Переопределяет [кбасекэйфраме:: аддтосторибоард](../../mfc/reference/cbasekeyframe-class.md#addtostoryboard).)|
|[Ккэйфраме:: Аддтосторибоардафтертранситион](#addtostoryboardaftertransition)|Добавляет опорный кадр в раскадровку после перехода.|
|[Ккэйфраме:: Аддтосторибоардатоффсет](#addtostoryboardatoffset)|Добавляет опорный кадр в раскадровку со смещением.|
|[Ккэйфраме:: Жетексистингкэйфраме](#getexistingkeyframe)|Возвращает указатель на опорный кадр, от которого зависит этот опорный кадр.|
|[Ккэйфраме:: offset](#getoffset)|Возвращает смещение от другого опорного кадра.|
|[Ккэйфраме:: ontransition](#gettransition)|Возвращает указатель на переход, от которого зависит этот опорный кадр.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[Ккэйфраме:: m_offset](#m_offset)|Задает смещение этого опорного кадра из опорного кадра, хранящегося в m_pExistingKeyFrame.|
|[Ккэйфраме:: m_pExistingKeyFrame](#m_pexistingkeyframe)|Хранит указатель на существующий кефраме. Этот опорный кадр добавляется в раскадровку с m_offset к существующему опорному кадру.|
|[Ккэйфраме:: m_pTransition](#m_ptransition)|Хранит указатель на перекрестие, которое начинается в этом опорном кадре.|

## <a name="remarks"></a>Комментарии

Этот класс реализует опорный кадр анимации. Ключевой кадр представляет момент времени в раскадровке и может использоваться для указания времени начала и окончания переходов. Опорный кадр может основываться на другом опорном кадре и иметь смещение (в секундах) от него или может быть основано на переходе и представлять момент времени, когда этот переход завершается.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[кбасекэйфраме](../../mfc/reference/cbasekeyframe-class.md)

[ккэйфраме](../../mfc/reference/ckeyframe-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="ckeyframeaddtostoryboard"></a><a name="addtostoryboard"></a> Ккэйфраме:: Аддтосторибоард

Добавляет опорный кадр в раскадровку.

```
virtual BOOL AddToStoryboard(
    IUIAnimationStoryboard* pStoryboard,
    BOOL bDeepAdd);
```

### <a name="parameters"></a>Параметры

*псторибоард*<br/>
Указатель на раскадровку.

*бдипадд*<br/>
Указывает, следует ли добавлять опорный кадр или переход рекурсивно.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если опорный кадр был успешно добавлен.

### <a name="remarks"></a>Комментарии

Этот метод добавляет опорный кадр в раскадровку. Если он зависит от другого опорного кадра или перехода, а Бдипадд имеет значение TRUE, этот метод пытается добавить их рекурсивно.

## <a name="ckeyframeaddtostoryboardaftertransition"></a><a name="addtostoryboardaftertransition"></a> Ккэйфраме:: Аддтосторибоардафтертранситион

Добавляет опорный кадр в раскадровку после перехода.

```
BOOL AddToStoryboardAfterTransition(
    IUIAnimationStoryboard* pStoryboard,
    BOOL bDeepAdd);
```

### <a name="parameters"></a>Параметры

*псторибоард*<br/>
Указатель на раскадровку.

*бдипадд*<br/>
Указывает, следует ли рекурсивно добавлять переходы.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если опорный кадр был успешно добавлен.

### <a name="remarks"></a>Комментарии

Эта функция вызывается платформой для добавления опорного кадра в раскадровку после перехода.

## <a name="ckeyframeaddtostoryboardatoffset"></a><a name="addtostoryboardatoffset"></a> Ккэйфраме:: Аддтосторибоардатоффсет

Добавляет опорный кадр в раскадровку со смещением.

```
virtual BOOL AddToStoryboardAtOffset(
    IUIAnimationStoryboard* pStoryboard,
    BOOL bDeepAdd);
```

### <a name="parameters"></a>Параметры

*псторибоард*<br/>
Указатель на раскадровку.

*бдипадд*<br/>
Указывает, следует ли добавить опорный кадр, который зависят от рекурсивного опорного кадра.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если опорный кадр был успешно добавлен.

### <a name="remarks"></a>Комментарии

Эта функция вызывается платформой для добавления опорного кадра в раскадровку со смещением.

## <a name="ckeyframeckeyframe"></a><a name="ckeyframe"></a> Ккэйфраме:: Ккэйфраме

Конструирует опорный кадр, зависящий от перехода.

```
CKeyFrame(CBaseTransition* pTransition);

CKeyFrame(
    CBaseKeyFrame* pKeyframe,
    UI_ANIMATION_SECONDS offset = 0.0);
```

### <a name="parameters"></a>Параметры

*птранситион*<br/>
Указатель на переход.

*Заданного параметром pKeyframe*<br/>
Указатель на опорный кадр.

*offset*<br/>
Смещение в секундах от опорного кадра, заданного параметром заданного параметром pKeyframe.

### <a name="remarks"></a>Комментарии

Созданный ключевой кадр будет представлять момент времени в раскадровке, когда заканчивается указанный переход.

## <a name="ckeyframegetexistingkeyframe"></a><a name="getexistingkeyframe"></a> Ккэйфраме:: Жетексистингкэйфраме

Возвращает указатель на опорный кадр, от которого зависит этот опорный кадр.

```
CBaseKeyFrame* GetExistingKeyframe();
```

### <a name="return-value"></a>Возвращаемое значение

Допустимый указатель на опорный кадр или значение NULL, если этот опорный кадр не зависит от другого опорного кадра.

### <a name="remarks"></a>Комментарии

Это метод доступа к опорному кадру, от которого зависит этот ключевой кадр.

## <a name="ckeyframegetoffset"></a><a name="getoffset"></a> Ккэйфраме:: offset

Возвращает смещение от другого опорного кадра.

```
UI_ANIMATION_SECONDS GetOffset();
```

### <a name="return-value"></a>Возвращаемое значение

Смещение в секундах от другого опорного кадра.

### <a name="remarks"></a>Комментарии

Этот метод следует вызывать для определения смещения в секундах от другого опорного кадра.

## <a name="ckeyframegettransition"></a><a name="gettransition"></a> Ккэйфраме:: ontransition

Возвращает указатель на переход, от которого зависит этот опорный кадр.

```
CBaseTransition* GetTransition();
```

### <a name="return-value"></a>Возвращаемое значение

Допустимый указатель на переход или значение NULL, если этот опорный кадр не зависит от перехода.

### <a name="remarks"></a>Комментарии

Это метод доступа к переходу, от которого зависит этот ключевой кадр.

## <a name="ckeyframem_offset"></a><a name="m_offset"></a> Ккэйфраме:: m_offset

Задает смещение этого опорного кадра из опорного кадра, хранящегося в m_pExistingKeyFrame.

```
UI_ANIMATION_SECONDS m_offset;
```

## <a name="ckeyframem_pexistingkeyframe"></a><a name="m_pexistingkeyframe"></a> Ккэйфраме:: m_pExistingKeyFrame

Хранит указатель на существующий кефраме. Этот опорный кадр добавляется в раскадровку с m_offset к существующему опорному кадру.

```
CBaseKeyFrame* m_pExistingKeyFrame;
```

## <a name="ckeyframem_ptransition"></a><a name="m_ptransition"></a> Ккэйфраме:: m_pTransition

Хранит указатель на перекрестие, которое начинается в этом опорном кадре.

```
CBaseTransition* m_pTransition;
```

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
