---
description: 'Дополнительные сведения о: Креверсалтранситион Class'
title: Класс CReversalTransition
ms.date: 11/04/2016
f1_keywords:
- CReversalTransition
- AFXANIMATIONCONTROLLER/CReversalTransition
- AFXANIMATIONCONTROLLER/CReversalTransition::CReversalTransition
- AFXANIMATIONCONTROLLER/CReversalTransition::Create
- AFXANIMATIONCONTROLLER/CReversalTransition::m_duration
helpviewer_keywords:
- CReversalTransition [MFC], CReversalTransition
- CReversalTransition [MFC], Create
- CReversalTransition [MFC], m_duration
ms.assetid: e89516be-2d07-4885-95a8-fc278f46e3ad
ms.openlocfilehash: f1d16562751e93ccf6df7ca3f70dac08bda8423d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97343011"
---
# <a name="creversaltransition-class"></a>Класс CReversalTransition

Инкапсулирует обратный переход.

## <a name="syntax"></a>Синтаксис

```
class CReversalTransition : public CBaseTransition;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Креверсалтранситион:: Креверсалтранситион](#creversaltransition)|Создает объект обратного перехода и инициализирует его длительность.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Креверсалтранситион:: Create](#create)|Вызывает библиотеку переходов для создания COM-объекта инкапсулированного перехода. (Переопределяет [CBaseTransition:: Create](../../mfc/reference/cbasetransition-class.md#create).)|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Креверсалтранситион:: m_duration](#m_duration)|Длительность перехода.|

## <a name="remarks"></a>Комментарии

Обратный переход плавно меняет направление в течение заданного промежутка времени. Конечное значение будет таким же, как исходное значение, а последняя скорость будет отрицательной на начальную скорость. Так как все переходы очищаются автоматически, рекомендуется выделять их с помощью оператора New. Инкапсулированный COM-объект Иуианиматионтранситион создается методом Каниматионконтроллер:: Аниматеграуп, пока он не будет равен NULL. Изменение переменных-членов после создания этого объекта COM не имеет силы.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CBaseTransition](../../mfc/reference/cbasetransition-class.md)

[креверсалтранситион](../../mfc/reference/creversaltransition-class.md)

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="creversaltransitioncreate"></a><a name="create"></a> Креверсалтранситион:: Create

Вызывает библиотеку переходов для создания COM-объекта инкапсулированного перехода.

```
virtual BOOL Create(
    IUIAnimationTransitionLibrary* pLibrary,
    IUIAnimationTransitionFactory* \*not used*\);
```

### <a name="parameters"></a>Параметры

*плибрари*<br/>
Указатель на библиотеку переходов, который отвечает за создание стандартных переходов.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если переход успешно создан; в противном случае — FALSE.

## <a name="creversaltransitioncreversaltransition"></a><a name="creversaltransition"></a> Креверсалтранситион:: Креверсалтранситион

Создает объект обратного перехода и инициализирует его длительность.

```
CReversalTransition(UI_ANIMATION_SECONDS duration);
```

### <a name="parameters"></a>Параметры

*duration*<br/>
Длительность перехода.

## <a name="creversaltransitionm_duration"></a><a name="m_duration"></a> Креверсалтранситион:: m_duration

Длительность перехода.

```
UI_ANIMATION_SECONDS m_duration;
```

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
