---
description: 'Дополнительные сведения о: Кмфкакцелераторкэй Class'
title: Класс Кмфкакцелераторкэй
ms.date: 11/04/2016
f1_keywords:
- CMFCAcceleratorKey
- AFXACCELERATORKEY/CMFCAcceleratorKey
- AFXACCELERATORKEY/CMFCAcceleratorKey::CMFCAcceleratorKey
- AFXACCELERATORKEY/CMFCAcceleratorKey::Format
- AFXACCELERATORKEY/CMFCAcceleratorKey::SetAccelerator
helpviewer_keywords:
- CMFCAcceleratorKey [MFC], CMFCAcceleratorKey
- CMFCAcceleratorKey [MFC], Format
- CMFCAcceleratorKey [MFC], SetAccelerator
ms.assetid: d140fbf7-23db-45ea-a63e-414a5ec7b3d5
ms.openlocfilehash: cb7fc24c4cb4d092c5f109ad892b3778d74a906f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336613"
---
# <a name="cmfcacceleratorkey-class"></a>Класс Кмфкакцелераторкэй

Вспомогательный класс, реализующий сопоставление и форматирование виртуальных ключей.

## <a name="syntax"></a>Синтаксис

```
class CMFCAcceleratorKey : public CObject
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кмфкакцелераторкэй:: Кмфкакцелераторкэй](#cmfcacceleratorkey)|Формирует объект `CMFCAcceleratorKey`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кмфкакцелераторкэй:: Format](#format)|Преобразует структуру рассрочки в визуальное представление.|
|[Кмфкакцелераторкэй:: Сетакцелератор](#setaccelerator)|Задает сочетание клавиш для `CMFCAcceleratorKey` объекта.|

## <a name="remarks"></a>Комментарии

Сочетания клавиш также называются клавишами быстрого доступа. Если вы хотите отобразить сочетания клавиш, введенные пользователем, [класс кмфкакцелераторкэйассигнктрл](../../mfc/reference/cmfcacceleratorkeyassignctrl-class.md) сопоставляет сочетания клавиш, такие как Alt + Shift + s, с пользовательским форматом текста, например "Alt + Shift + s". Каждый `CMFCAcceleratorKey` объект сопоставляет один сочетание клавиш с текстовым форматом.

Дополнительные сведения об использовании сочетаний клавиш и таблиц сочетаний клавиш см. в разделе [класс CKeyboardManager](../../mfc/reference/ckeyboardmanager-class.md).

## <a name="example"></a>Пример

В следующем примере показано, как создать `CMFCAcceleratorKey` объект и как использовать его `Format` метод.

[!code-cpp[NVC_MFC_RibbonApp#30](../../mfc/reference/codesnippet/cpp/cmfcacceleratorkey-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CMFCAcceleratorKey`

## <a name="requirements"></a>Требования

**Заголовок:** афксакцелераторкэй. h

## <a name="cmfcacceleratorkeycmfcacceleratorkey"></a><a name="cmfcacceleratorkey"></a> Кмфкакцелераторкэй:: Кмфкакцелераторкэй

Конструирует объект [кмфкакцелераторкэй](../../mfc/reference/cmfcacceleratorkey-class.md) .

```
CMFCAcceleratorKey();
CMFCAcceleratorKey(LPACCEL lpAccel);
```

### <a name="parameters"></a>Параметры

*лпакцел*<br/>
окне Указатель на сочетание клавиш.

### <a name="remarks"></a>Комментарии

Если не указать сочетание клавиш при создании `CMFCAccleratorKey` , используйте метод [кмфкакцелераторкэй:: сетакцелератор](#setaccelerator) , чтобы связать сочетание клавиш с `CMFCAcceleratorKey` объектом.

## <a name="cmfcacceleratorkeyformat"></a><a name="format"></a> Кмфкакцелераторкэй:: Format

Преобразует структуру рассрочки в связанное строковое значение.

```cpp
void Format(CString& str) const;
```

### <a name="parameters"></a>Параметры

*str*<br/>
заполняет Ссылка на объект, в `CString` котором метод записывает преобразованную комбинацию клавиш.

### <a name="remarks"></a>Комментарии

Этот метод извлекает формат строки для связанного сочетания клавиш. Можно задать формат строки для объекта [кмфкакцелераторкэй](../../mfc/reference/cmfcacceleratorkey-class.md) с помощью конструктора или метода [Кмфкакцелераторкэй:: сетакцелератор](#setaccelerator).

## <a name="cmfcacceleratorkeysetaccelerator"></a><a name="setaccelerator"></a> Кмфкакцелераторкэй:: Сетакцелератор

Задает сочетание клавиш для объекта [кмфкакцелераторкэй](../../mfc/reference/cmfcacceleratorkey-class.md) .

```cpp
void SetAccelerator(LPACCEL lpAccel);
```

### <a name="parameters"></a>Параметры

*лпакцел*<br/>
окне Указатель на сочетание клавиш.

### <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы задать сочетание клавиш для, `CMFCAcceleratorKey` Если вы не указали сочетание клавиш при создании `CMFCAcceleratorKey` .

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CKeyboardManager](../../mfc/reference/ckeyboardmanager-class.md)
