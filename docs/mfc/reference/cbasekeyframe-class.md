---
description: 'Дополнительные сведения о: Кбасекэйфраме Class'
title: Класс CBaseKeyFrame
ms.date: 11/04/2016
f1_keywords:
- CBaseKeyFrame
- AFXANIMATIONCONTROLLER/CBaseKeyFrame
- AFXANIMATIONCONTROLLER/CBaseKeyFrame::CBaseKeyFrame
- AFXANIMATIONCONTROLLER/CBaseKeyFrame::AddToStoryboard
- AFXANIMATIONCONTROLLER/CBaseKeyFrame::GetAnimationKeyframe
- AFXANIMATIONCONTROLLER/CBaseKeyFrame::IsAdded
- AFXANIMATIONCONTROLLER/CBaseKeyFrame::IsKeyframeAtOffset
- AFXANIMATIONCONTROLLER/CBaseKeyFrame::m_bAdded
- AFXANIMATIONCONTROLLER/CBaseKeyFrame::m_bIsKeyframeAtOffset
- AFXANIMATIONCONTROLLER/CBaseKeyFrame::m_keyframe
helpviewer_keywords:
- CBaseKeyFrame [MFC], CBaseKeyFrame
- CBaseKeyFrame [MFC], AddToStoryboard
- CBaseKeyFrame [MFC], GetAnimationKeyframe
- CBaseKeyFrame [MFC], IsAdded
- CBaseKeyFrame [MFC], IsKeyframeAtOffset
- CBaseKeyFrame [MFC], m_bAdded
- CBaseKeyFrame [MFC], m_bIsKeyframeAtOffset
- CBaseKeyFrame [MFC], m_keyframe
ms.assetid: 285a2eff-e7c4-43be-b5aa-737727e6866d
ms.openlocfilehash: 0bebd91183eab9be71e8df4928dc621565718cb9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97261261"
---
# <a name="cbasekeyframe-class"></a>Класс CBaseKeyFrame

Реализует базовую функциональность ключевого кадра.

## <a name="syntax"></a>Синтаксис

```
class CBaseKeyFrame : public CObject;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кбасекэйфраме:: Кбасекэйфраме](#cbasekeyframe)|Конструирует объект опорного кадра.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кбасекэйфраме:: Аддтосторибоард](#addtostoryboard)|Добавляет опорный кадр в раскадровку.|
|[Кбасекэйфраме:: Жетаниматионкэйфраме](#getanimationkeyframe)|Возвращает значение базового опорного кадра.|
|[Кбасекэйфраме:: added](#isadded)|Сообщает, добавлен ли опорный кадр в раскадровку.|
|[Кбасекэйфраме:: Искэйфрамеатоффсет](#iskeyframeatoffset)|Указывает, следует ли добавлять опорный кадр в раскадровку со смещением или после перехода.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[Кбасекэйфраме:: m_bAdded](#m_badded)|Указывает, добавлен ли этот опорный кадр в раскадровку.|
|[Кбасекэйфраме:: m_bIsKeyframeAtOffset](#m_biskeyframeatoffset)|Указывает, следует ли добавлять этот опорный кадр в раскадровку со смещением от другого существующего опорного кадра или в конце некоторого перехода.|
|[Кбасекэйфраме:: m_keyframe](#m_keyframe)|Представляет ключевой кадр API анимации Windows. Если опорный кадр не инициализирован, ему присваивается предопределенное значение UI_ANIMATION_KEYFRAME_STORYBOARD_START.|

## <a name="remarks"></a>Комментарии

Инкапсулирует UI_ANIMATION_KEYFRAME переменную. Служит базовым классом для любой реализации опорного кадра. Ключевой кадр представляет момент времени в раскадровке и может использоваться для указания времени начала и окончания переходов. Существует два типа опорных кадров: опорные кадры, добавленные в раскадровку по заданному смещению (по времени) или опорные кадры, добавленные после указанного перехода. Так как длительность некоторых переходов не может быть известна до начала анимации, фактические значения некоторых опорных кадров определяются только во время выполнения. Поскольку ключевые кадры могут зависеть от переходов, которые, в свою очередь, зависят от ключевых кадров, важно предотвратить бесконечные рекурсия при построении цепочек ключевых кадров.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CBaseKeyFrame`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="cbasekeyframeaddtostoryboard"></a><a name="addtostoryboard"></a> Кбасекэйфраме:: Аддтосторибоард

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
Если этот параметр имеет значение TRUE и добавляемый опорный кадр зависит от какого-либо другого опорного кадра или перехода, этот метод пытается добавить этот ключевой кадр или перейти в раскадровку в первую очередь.

### <a name="return-value"></a>Возвращаемое значение

TRUE, если опорный кадр был успешно добавлен в раскадровку; в противном случае — FALSE.

### <a name="remarks"></a>Комментарии

Этот метод вызывается для добавления опорного кадра в раскадровку.

## <a name="cbasekeyframecbasekeyframe"></a><a name="cbasekeyframe"></a> Кбасекэйфраме:: Кбасекэйфраме

Конструирует объект опорного кадра.

```
CBaseKeyFrame();
```

## <a name="cbasekeyframegetanimationkeyframe"></a><a name="getanimationkeyframe"></a> Кбасекэйфраме:: Жетаниматионкэйфраме

Возвращает значение базового опорного кадра.

```
UI_ANIMATION_KEYFRAME GetAnimationKeyframe() const;
```

### <a name="return-value"></a>Возвращаемое значение

Текущий опорный кадр. Значение по умолчанию — UI_ANIMATION_KEYFRAME_STORYBOARD_START.

### <a name="remarks"></a>Комментарии

Это метод доступа к значению базового опорного кадра.

## <a name="cbasekeyframeisadded"></a><a name="isadded"></a> Кбасекэйфраме:: added

Сообщает, добавлен ли опорный кадр в раскадровку.

```
BOOL IsAdded() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если опорный кадр добавлен в раскадровку; противном случае — FALSE.

### <a name="remarks"></a>Комментарии

В базовом классе функция added всегда возвращает значение TRUE, но переопределяется в производных классах.

## <a name="cbasekeyframeiskeyframeatoffset"></a><a name="iskeyframeatoffset"></a> Кбасекэйфраме:: Искэйфрамеатоффсет

Указывает, следует ли добавлять опорный кадр в раскадровку со смещением или после перехода.

```
BOOL IsKeyframeAtOffset() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если опорный кадр должен быть добавлен в раскадровку с некоторым указанным смещением. Значение FALSE, если опорный кадр должен быть добавлен в раскадровку после некоторого перехода.

### <a name="remarks"></a>Комментарии

Указывает, следует ли добавлять опорный кадр в раскадровку со смещением. Смещение или переход должны быть указаны в производном классе.

## <a name="cbasekeyframem_badded"></a><a name="m_badded"></a> Кбасекэйфраме:: m_bAdded

Указывает, добавлен ли этот опорный кадр в раскадровку.

```
BOOL m_bAdded;
```

## <a name="cbasekeyframem_biskeyframeatoffset"></a><a name="m_biskeyframeatoffset"></a> Кбасекэйфраме:: m_bIsKeyframeAtOffset

Указывает, следует ли добавлять этот опорный кадр в раскадровку со смещением от другого существующего опорного кадра или в конце некоторого перехода.

```
BOOL m_bIsKeyframeAtOffset;
```

## <a name="cbasekeyframem_keyframe"></a><a name="m_keyframe"></a> Кбасекэйфраме:: m_keyframe

Представляет ключевой кадр API анимации Windows. Если опорный кадр не инициализирован, ему присваивается предопределенное значение UI_ANIMATION_KEYFRAME_STORYBOARD_START.

```
UI_ANIMATION_KEYFRAME m_keyframe;
```

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
