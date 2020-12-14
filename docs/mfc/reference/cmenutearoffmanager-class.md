---
description: 'Дополнительные сведения о: Кменутеароффманажер Class'
title: Класс Кменутеароффманажер
ms.date: 10/18/2018
f1_keywords:
- CMenuTearOffManager
- AFXMENUTEAROFFMANAGER/CMenuTearOffManager
- AFXMENUTEAROFFMANAGER/CMenuTearOffManager::CMenuTearOffManager
- AFXMENUTEAROFFMANAGER/CMenuTearOffManager::Build
- AFXMENUTEAROFFMANAGER/CMenuTearOffManager::GetRegPath
- AFXMENUTEAROFFMANAGER/CMenuTearOffManager::Initialize
- AFXMENUTEAROFFMANAGER/CMenuTearOffManager::IsDynamicID
- AFXMENUTEAROFFMANAGER/CMenuTearOffManager::Parse
- AFXMENUTEAROFFMANAGER/CMenuTearOffManager::Reset
- AFXMENUTEAROFFMANAGER/CMenuTearOffManager::SetInUse
- AFXMENUTEAROFFMANAGER/CMenuTearOffManager::SetupTearOffMenus
helpviewer_keywords:
- CMenuTearOffManager [MFC], CMenuTearOffManager
- CMenuTearOffManager [MFC], Build
- CMenuTearOffManager [MFC], GetRegPath
- CMenuTearOffManager [MFC], Initialize
- CMenuTearOffManager [MFC], IsDynamicID
- CMenuTearOffManager [MFC], Parse
- CMenuTearOffManager [MFC], Reset
- CMenuTearOffManager [MFC], SetInUse
- CMenuTearOffManager [MFC], SetupTearOffMenus
ms.assetid: ab7ca272-ce42-4678-95f7-6ad75038f5a0
ms.openlocfilehash: b80f2e935f8d1dd47bf19a11522e4556b35490b4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336640"
---
# <a name="cmenutearoffmanager-class"></a>Класс Кменутеароффманажер

Управление перемещаемыми меню. Перемещаемое меню — это меню в строке меню. Пользователь может удалить перемещаемое меню из строки меню, превращая перемещаемое меню в плавающее.

   Дополнительные сведения см. в исходном коде, расположенном в папке **VC \\ атлмфк \\ src \\ MFC** в установке Visual Studio.

## <a name="syntax"></a>Синтаксис

```
class CMenuTearOffManager : public CObject
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кменутеароффманажер:: Кменутеароффманажер](#cmenutearoffmanager)|Формирует объект `CMenuTearOffManager`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кменутеароффманажер:: Build](#build)||
|[Кменутеароффманажер:: Жетрегпас](#getregpath)||
|[Кменутеароффманажер:: Initialize](#initialize)|Инициализирует объект `CMenuTearOffManager`.|
|[Кменутеароффманажер:: ИсдинамиЦид](#isdynamicid)||
|[Кменутеароффманажер::P Арсе](#parse)||
|[Кменутеароффманажер:: Reset](#reset)||
|[Кменутеароффманажер:: Сетинусе](#setinuse)||
|[Кменутеароффманажер:: Сетуптеароффменус](#setuptearoffmenus)||

## <a name="remarks"></a>Комментарии

Чтобы использовать в приложении меню с отрывным выходом, необходимо иметь `CMenuTearOffManager` объект. В большинстве случаев объект не создается и не инициализируется `CMenuTearOffManager` напрямую. Он обрабатывается при вызове функции [CWinAppEx:: енаблетеароффменус](../../mfc/reference/cwinappex-class.md#enabletearoffmenus) .

## <a name="example"></a>Пример

В следующем примере показано, как создать и инициализировать `CMenuTearOffManager` объект, вызвав `CWinAppEX::EnableTearOffMenus` метод. Этот фрагмент кода входит в состав [примера Word Pad](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_WordPad#12](../../mfc/reference/codesnippet/cpp/cmenutearoffmanager-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CMenuTearOffManager`

## <a name="requirements"></a>Требования

**Заголовок:** афксменутеароффманажер. h

## <a name="cmenutearoffmanagerbuild"></a><a name="build"></a> Кменутеароффманажер:: Build

```cpp
void Build(
    UINT uiTearOffBarID,
    CString& strText);
```

### <a name="parameters"></a>Параметры

окне *уитеароффбарид*<br/>

окне *стртекст*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmenutearoffmanagercmenutearoffmanager"></a><a name="cmenutearoffmanager"></a> Кменутеароффманажер:: Кменутеароффманажер

Конструирует объект [кменутеароффманажер](../../mfc/reference/cmenutearoffmanager-class.md) .

```
CMenuTearOffManager();
```

### <a name="remarks"></a>Комментарии

В большинстве случаев не следует создавать `CMenuTearOffManager` вручную. Платформа приложения создает `CMenuTearOffManager` объект при вызове [CWinAppEx:: енаблетеароффменус](../../mfc/reference/cwinappex-class.md#enabletearoffmenus).

## <a name="cmenutearoffmanagergetregpath"></a><a name="getregpath"></a> Кменутеароффманажер:: Жетрегпас

```
LPCTSTR GetRegPath() const;
```

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmenutearoffmanagerinitialize"></a><a name="initialize"></a> Кменутеароффманажер:: Initialize

Инициализирует объект [кменутеароффманажер](../../mfc/reference/cmenutearoffmanager-class.md) .

```
BOOL Initialize(
    LPCTSTR lpszRegEntry,
    UINT uiTearOffMenuFirst,
    UINT uiTearOffMenuLast);
```

### <a name="parameters"></a>Параметры

*лпсзрежентри*<br/>
окне Строка, содержащая путь к записи реестра. Приложения сохраняют параметры для отрезков в этой записи реестра.

*уитеароффменуфирст*<br/>
окне Первый идентификатор меню для отрезкиного меню.

*уитеароффменуласт*<br/>
окне Последний идентификатор меню для отрывного меню.

### <a name="return-value"></a>Возвращаемое значение

Имеет ненулевое значение в случае успешного выполнения, иначе — 0.

### <a name="remarks"></a>Комментарии

Диапазон идентификаторов меню из *уитеароффменуфирст* в *уитеароффменуласт* должен быть непрерывным интервалом. Интервал определяет количество неразрывных меню, которые могут одновременно отображаться в приложении.

## <a name="cmenutearoffmanagerisdynamicid"></a><a name="isdynamicid"></a> Кменутеароффманажер:: ИсдинамиЦид

```
BOOL IsDynamicID(UINT uiID) const;
```

### <a name="parameters"></a>Параметры

окне *уиид*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmenutearoffmanagerparse"></a><a name="parse"></a> Кменутеароффманажер::P Арсе

```
UINT Parse(CString& str);
```

### <a name="parameters"></a>Параметры

окне *str*<br/>

### <a name="return-value"></a>Возвращаемое значение

### <a name="remarks"></a>Комментарии

## <a name="cmenutearoffmanagerreset"></a><a name="reset"></a> Кменутеароффманажер:: Reset

```cpp
void Reset(HMENU hmenu);
```

### <a name="parameters"></a>Параметры

окне *HMENU*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmenutearoffmanagersetinuse"></a><a name="setinuse"></a> Кменутеароффманажер:: Сетинусе

```cpp
void SetInUse(
    UINT uiCmdId,
    BOOL bUse = TRUE);
```

### <a name="parameters"></a>Параметры

окне *уикмдид*<br/>

окне *бусе*<br/>

### <a name="remarks"></a>Комментарии

## <a name="cmenutearoffmanagersetuptearoffmenus"></a><a name="setuptearoffmenus"></a> Кменутеароффманажер:: Сетуптеароффменус

```cpp
void SetupTearOffMenus(HMENU hMenu);
```

### <a name="parameters"></a>Параметры

окне *HMENU*<br/>

### <a name="remarks"></a>Комментарии

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CWinAppEx](../../mfc/reference/cwinappex-class.md)
