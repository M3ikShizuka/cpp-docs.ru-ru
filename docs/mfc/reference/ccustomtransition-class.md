---
description: 'Дополнительные сведения о: Ккустомтранситион Class'
title: Класс CCustomTransition
ms.date: 11/04/2016
f1_keywords:
- CCustomTransition
- AFXANIMATIONCONTROLLER/CCustomTransition
- AFXANIMATIONCONTROLLER/CCustomTransition::CCustomTransition
- AFXANIMATIONCONTROLLER/CCustomTransition::Create
- AFXANIMATIONCONTROLLER/CCustomTransition::SetInitialValue
- AFXANIMATIONCONTROLLER/CCustomTransition::SetInitialVelocity
- AFXANIMATIONCONTROLLER/CCustomTransition::m_bInitialValueSpecified
- AFXANIMATIONCONTROLLER/CCustomTransition::m_bInitialVelocitySpecified
- AFXANIMATIONCONTROLLER/CCustomTransition::m_initialValue
- AFXANIMATIONCONTROLLER/CCustomTransition::m_initialVelocity
- AFXANIMATIONCONTROLLER/CCustomTransition::m_pInterpolator
helpviewer_keywords:
- CCustomTransition [MFC], CCustomTransition
- CCustomTransition [MFC], Create
- CCustomTransition [MFC], SetInitialValue
- CCustomTransition [MFC], SetInitialVelocity
- CCustomTransition [MFC], m_bInitialValueSpecified
- CCustomTransition [MFC], m_bInitialVelocitySpecified
- CCustomTransition [MFC], m_initialValue
- CCustomTransition [MFC], m_initialVelocity
- CCustomTransition [MFC], m_pInterpolator
ms.assetid: 5bd3f492-940f-4290-a38b-fa68eb8f8401
ms.openlocfilehash: 22c08cdcedc3a7cbdbe824ac1d98d62cfe810772
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97227667"
---
# <a name="ccustomtransition-class"></a>Класс CCustomTransition

Реализует пользовательский переход.

## <a name="syntax"></a>Синтаксис

```
class CCustomTransition : public CBaseTransition;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккустомтранситион:: Ккустомтранситион](#ccustomtransition)|Конструирует пользовательский объект перехода.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккустомтранситион:: Create](#create)|Вызывает библиотеку переходов для создания COM-объекта инкапсулированного перехода. (Переопределяет [CBaseTransition:: Create](../../mfc/reference/cbasetransition-class.md#create).)|
|[Ккустомтранситион:: Сетинитиалвалуе](#setinitialvalue)|Задает начальное значение, которое будет применено к переменной анимации, связанной с этим переходом.|
|[Ккустомтранситион:: СетинитиалвелоЦити](#setinitialvelocity)|Задает начальную скорость, которая будет применена к переменной анимации, связанной с этим переходом.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[Ккустомтранситион:: m_bInitialValueSpecified](#m_binitialvaluespecified)|Указывает, было ли начальное значение указано с помощью Сетинитиалвалуе.|
|[Ккустомтранситион:: m_bInitialVelocitySpecified](#m_binitialvelocityspecified)|Указывает, была ли Начальная скорость указана с помощью СетинитиалвелоЦити.|
|[Ккустомтранситион:: m_initialValue](#m_initialvalue)|Сохраняет начальное значение.|
|[Ккустомтранситион:: m_initialVelocity](#m_initialvelocity)|Сохраняет начальную скорость.|
|[Ккустомтранситион:: m_pInterpolator](#m_pinterpolator)|Хранит указатель на пользовательский интерполяцию.|

## <a name="remarks"></a>Комментарии

Класс Ккустомтранситионс позволяет разработчикам реализовывать пользовательские переходы. Он создается и используется в качестве стандартного перехода, но его конструктор принимает в качестве параметра указатель на настраиваемый интерполяцию. Выполните следующие действия, чтобы использовать пользовательские переходы: 1. Создайте класс, производный от Ккустоминтерполатор, и реализуйте по крайней мере метод Интерполатевалуе. 2. Убедитесь, что время существования пользовательского объекта интерполяции должно быть дольше, чем длительность анимации, в которой он используется. 3. Создание экземпляра (с помощью оператора New) объекта Ккустомтранситион и передача указателя пользовательскому интерполяции в конструкторе. 4. Вызовите Ккустомтранситион:: Сетинитиалвалуе и Ккустомтранситион:: СетинитиалвелоЦити, если эти параметры необходимы для пользовательской интерполяции. 5. Передайте указатель на пользовательский переход к методу Аддтранситион объекта анимации, значение которого должно быть анимировано с помощью пользовательского алгоритма. 6. Когда значение объекта анимации должно изменить API анимации Windows, будет вызывать Интерполатевалуе (и другие соответствующие методы) в Ккустоминтерполатор.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CBaseTransition](../../mfc/reference/cbasetransition-class.md)

`CCustomTransition`

## <a name="requirements"></a>Требования

**Заголовок:** afxanimationcontroller.h

## <a name="ccustomtransitionccustomtransition"></a><a name="ccustomtransition"></a> Ккустомтранситион:: Ккустомтранситион

Конструирует пользовательский объект перехода.

```
CCustomTransition(CCustomInterpolator* pInterpolator);
```

### <a name="parameters"></a>Параметры

*пинтерполатор*<br/>
Указатель на настраиваемый интерполяцию.

## <a name="ccustomtransitioncreate"></a><a name="create"></a> Ккустомтранситион:: Create

Вызывает библиотеку переходов для создания COM-объекта инкапсулированного перехода.

```
virtual BOOL Create(
    IUIAnimationTransitionLibrary* */,
    IUIAnimationTransitionFactory* pFactory);
```

### <a name="parameters"></a>Параметры

*pFactory*<br/>
Указатель на фабрику переходов, который отвечает за создание пользовательских переходов.

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

Этот метод также позволяет задать начальное и начальное значение скорости для переменной анимации, связанной с этим переходом. Для этой цели необходимо вызвать Сетинитиалвалуе и СетинитиалвелоЦити, прежде чем платформа создаст объект COM для инкапсулированного перехода (это происходит при вызове Каниматионконтроллер:: Аниматеграуп).

## <a name="ccustomtransitionm_binitialvaluespecified"></a><a name="m_binitialvaluespecified"></a> Ккустомтранситион:: m_bInitialValueSpecified

Указывает, было ли начальное значение указано с помощью Сетинитиалвалуе.

```
BOOL m_bInitialValueSpecified;
```

## <a name="ccustomtransitionm_binitialvelocityspecified"></a><a name="m_binitialvelocityspecified"></a> Ккустомтранситион:: m_bInitialVelocitySpecified

Указывает, была ли Начальная скорость указана с помощью СетинитиалвелоЦити.

```
BOOL m_bInitialVelocitySpecified;
```

## <a name="ccustomtransitionm_initialvalue"></a><a name="m_initialvalue"></a> Ккустомтранситион:: m_initialValue

Сохраняет начальное значение.

```
DOUBLE m_initialValue;
```

## <a name="ccustomtransitionm_initialvelocity"></a><a name="m_initialvelocity"></a> Ккустомтранситион:: m_initialVelocity

Сохраняет начальную скорость.

```
DOUBLE m_initialVelocity;
```

## <a name="ccustomtransitionm_pinterpolator"></a><a name="m_pinterpolator"></a> Ккустомтранситион:: m_pInterpolator

Хранит указатель на пользовательский интерполяцию.

```
CCustomInterpolator* m_pInterpolator;
```

## <a name="ccustomtransitionsetinitialvalue"></a><a name="setinitialvalue"></a> Ккустомтранситион:: Сетинитиалвалуе

Задает начальное значение, которое будет применено к переменной анимации, связанной с этим переходом.

```cpp
void SetInitialValue(DOUBLE initialValue);
```

### <a name="parameters"></a>Параметры

*инитиалвалуе*

## <a name="ccustomtransitionsetinitialvelocity"></a><a name="setinitialvelocity"></a> Ккустомтранситион:: СетинитиалвелоЦити

Задает начальную скорость, которая будет применена к переменной анимации, связанной с этим переходом.

```cpp
void SetInitialVelocity(DOUBLE initialVelocity);
```

### <a name="parameters"></a>Параметры

*InitialVelocity равно*

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
