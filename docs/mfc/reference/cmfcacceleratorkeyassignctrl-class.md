---
description: 'Дополнительные сведения о: Кмфкакцелераторкэйассигнктрл Class'
title: Класс CMFCAcceleratorKeyAssignCtrl
ms.date: 10/18/2018
f1_keywords:
- CMFCAcceleratorKeyAssignCtrl
- AFXACCELERATORKEYASSIGNCTRL/CMFCAcceleratorKeyAssignCtrl
- AFXACCELERATORKEYASSIGNCTRL/CMFCAcceleratorKeyAssignCtrl::CMFCAcceleratorKeyAssignCtrl
- AFXACCELERATORKEYASSIGNCTRL/CMFCAcceleratorKeyAssignCtrl::GetAccel
- AFXACCELERATORKEYASSIGNCTRL/CMFCAcceleratorKeyAssignCtrl::IsFocused
- AFXACCELERATORKEYASSIGNCTRL/CMFCAcceleratorKeyAssignCtrl::IsKeyDefined
- AFXACCELERATORKEYASSIGNCTRL/CMFCAcceleratorKeyAssignCtrl::PreTranslateMessage
- AFXACCELERATORKEYASSIGNCTRL/CMFCAcceleratorKeyAssignCtrl::ResetKey
helpviewer_keywords:
- CMFCAcceleratorKeyAssignCtrl [MFC], CMFCAcceleratorKeyAssignCtrl
- CMFCAcceleratorKeyAssignCtrl [MFC], GetAccel
- CMFCAcceleratorKeyAssignCtrl [MFC], IsFocused
- CMFCAcceleratorKeyAssignCtrl [MFC], IsKeyDefined
- CMFCAcceleratorKeyAssignCtrl [MFC], PreTranslateMessage
- CMFCAcceleratorKeyAssignCtrl [MFC], ResetKey
ms.assetid: 89fb8e62-596e-4e71-8c9a-32740347aaab
ms.openlocfilehash: 0f5584dfa521f45841691bff3775d9cd98808b9a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336587"
---
# <a name="cmfcacceleratorkeyassignctrl-class"></a>Класс CMFCAcceleratorKeyAssignCtrl

`CMFCAcceleratorKeyAssignCtrl`Класс расширяет [класс CEdit](../../mfc/reference/cedit-class.md) для поддержки дополнительных системных кнопок, таких как Alt, Control и Shift.

## <a name="syntax"></a>Синтаксис

```
class CMFCAcceleratorKeyAssignCtrl : public CEdit
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CMFCAcceleratorKeyAssignCtrl::CMFCAcceleratorKeyAssignCtrl](#cmfcacceleratorkeyassignctrl)|Формирует объект `CMFCAcceleratorKeyAssignCtrl`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CMFCAcceleratorKeyAssignCtrl::GetAccel](#getaccel)|Извлекает `ACCEL` структуру для сочетания клавиш, нажатого в объекте `CMFCAcceleratorKeyAssignCtrl`.|
|[Кмфкакцелераторкэйассигнктрл:: с фокусом](#isfocused)||
|[CMFCAcceleratorKeyAssignCtrl::IsKeyDefined](#iskeydefined)|Определяет, задано ли сочетание клавиш.|
|[CMFCAcceleratorKeyAssignCtrl::PreTranslateMessage](#pretranslatemessage)|Используется классом [CWinApp](../../mfc/reference/cwinapp-class.md) для преобразования сообщений окна перед их передачей функциям Windows [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage) и [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) . (Переопределяет [CWnd::PreTranslateMessage](../../mfc/reference/cwnd-class.md#pretranslatemessage).)|
|[CMFCAcceleratorKeyAssignCtrl::ResetKey](#resetkey)|Сбрасывает сочетание клавиш.|

## <a name="remarks"></a>Комментарии

Этот класс расширяет функциональность класса `CEdit` благодаря поддержке сочетаний клавиш. `CMFCAcceleratorKeyAssignCtrl`Класс функционирует как [класс CEdit](../../mfc/reference/cedit-class.md) и может также распознать системные кнопки.

Этот класс сопоставляет физические сочетания клавиш со строковыми значениями. Например, пусть сочетание клавиш ALT+B сопоставлено со строкой "Alt + B". Когда пользователь нажимает это сочетание клавиш в объекте `CMFCAcceleratorKeyAssignCtrl`, отображается строка "Alt + B". Дополнительные сведения о сопоставлении сочетаний клавиш и формата строки см. в разделе [класс кмфкакцелераторкэй](../../mfc/reference/cmfcacceleratorkey-class.md).

## <a name="example"></a>Пример

В этом примере демонстрируется создание объекта `CMFCAcceleratorKeyAssignCtrl` и использование его метода `ResetKey` для сброса сочетания клавиш.

[!code-cpp[NVC_MFC_RibbonApp#31](../../mfc/reference/codesnippet/cpp/cmfcacceleratorkeyassignctrl-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CEdit](../../mfc/reference/cedit-class.md)

`CMFCAcceleratorKeyAssignCtrl`

## <a name="requirements"></a>Требования

**Заголовок:** афксакцелераторкэйассигнктрл. h

## <a name="cmfcacceleratorkeyassignctrlcmfcacceleratorkeyassignctrl"></a><a name="cmfcacceleratorkeyassignctrl"></a> Кмфкакцелераторкэйассигнктрл:: Кмфкакцелераторкэйассигнктрл

Конструирует объект [кмфкакцелераторкэйассигнктрл](../../mfc/reference/cmfcacceleratorkeyassignctrl-class.md) .

```
CMFCAcceleratorKeyAssignCtrl();
```

## <a name="cmfcacceleratorkeyassignctrlgetaccel"></a><a name="getaccel"></a> Кмфкакцелераторкэйассигнктрл:: i

Извлекает `ACCEL` структуру сочетания клавиш, нажатой в объекте [кмфкакцелераторкэйассигнктрл](../../mfc/reference/cmfcacceleratorkeyassignctrl-class.md) .

```
ACCEL const* GetAccel() const;
```

### <a name="return-value"></a>Возвращаемое значение

`ACCEL`Структура, описывающая сочетание клавиш.

### <a name="remarks"></a>Комментарии

Эта функция используется для получения `ACCEL` структуры сочетания клавиш, вводимых пользователем в `CMFCAcceleratorKeyAssignCtrl` объект.

## <a name="cmfcacceleratorkeyassignctrlisfocused"></a><a name="isfocused"></a> Кмфкакцелераторкэйассигнктрл:: с фокусом

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
BOOL IsFocused() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcacceleratorkeyassignctrliskeydefined"></a><a name="iskeydefined"></a> Кмфкакцелераторкэйассигнктрл:: Искэйдефинед

Определяет, определен ли в объекте [кмфкакцелераторкэйассигнктрл](../../mfc/reference/cmfcacceleratorkeyassignctrl-class.md) сочетание клавиш.

```
BOOL IsKeyDefined() const;
```

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если пользователь уже нажал на допустимое сочетание ключей, определяющих сочетание клавиш; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Эта функция используется для определения того, вошел ли пользователь в объект в качестве допустимого сочетания клавиш `CMFCAcceleratorKeyAssignCtrl` . Если сочетание клавиш существует, можно использовать метод [кмфкакцелераторкэйассигнктрл::](#getaccel) , чтобы получить `ACCEL` структуру, связанную с этим сочетанием клавиш.

## <a name="cmfcacceleratorkeyassignctrlpretranslatemessage"></a><a name="pretranslatemessage"></a> Кмфкакцелераторкэйассигнктрл::P Ретранслатемессаже

Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

```
virtual BOOL PreTranslateMessage(MSG* pMsg);
```

### <a name="parameters"></a>Параметры

[in] *pMsg*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmfcacceleratorkeyassignctrlresetkey"></a><a name="resetkey"></a> Кмфкакцелераторкэйассигнктрл:: Ресеткэй

Сбрасывает сочетание клавиш.

```cpp
void ResetKey();
```

### <a name="remarks"></a>Комментарии

Функция очищает текст элемента управления Edit. Сюда входят все сочетания клавиш, нажатые пользователем.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс Кмфкакцелераторкэй](../../mfc/reference/cmfcacceleratorkey-class.md)
