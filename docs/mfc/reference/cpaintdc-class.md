---
description: 'Дополнительные сведения о: Кпаинтдк Class'
title: Класс Кпаинтдк
ms.date: 11/04/2016
f1_keywords:
- CPaintDC
- AFXWIN/CPaintDC
- AFXWIN/CPaintDC::CPaintDC
- AFXWIN/CPaintDC::m_ps
- AFXWIN/CPaintDC::m_hWnd
helpviewer_keywords:
- CPaintDC [MFC], CPaintDC
- CPaintDC [MFC], m_ps
- CPaintDC [MFC], m_hWnd
ms.assetid: 7e245baa-bf9b-403e-a637-7218adf28fab
ms.openlocfilehash: cb8f3b81615390ab6af8e9a244a95f91a3b3f96c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97345216"
---
# <a name="cpaintdc-class"></a>Класс Кпаинтдк

Класс контекста устройства, производный от [CDC](../../mfc/reference/cdc-class.md).

## <a name="syntax"></a>Синтаксис

```
class CPaintDC : public CDC
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кпаинтдк:: Кпаинтдк](#cpaintdc)|Конструирует объект, `CPaintDC` подключенный к заданному [CWnd](../../mfc/reference/cwnd-class.md).|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Кпаинтдк:: m_ps](#m_ps)|Содержит [PAINTSTRUCT](/windows/win32/api/winuser/ns-winuser-paintstruct) , используемый для рисования клиентской области.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[Кпаинтдк:: m_hWnd](#m_hwnd)|HWND, к которому `CPaintDC` присоединен этот объект.|

## <a name="remarks"></a>Комментарии

Он выполняет [CWnd:: бегинпаинт](../../mfc/reference/cwnd-class.md#beginpaint) во время создания и [CWnd:: ендпаинт](../../mfc/reference/cwnd-class.md#endpaint) во время уничтожения.

`CPaintDC`Объект может использоваться только при ответе на сообщение [WM_PAINT](/windows/win32/gdi/wm-paint) , обычно в `OnPaint` функции-члене обработчика сообщений.

Дополнительные сведения об использовании см `CPaintDC` . в разделе [контексты устройств](../../mfc/device-contexts.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CDC](../../mfc/reference/cdc-class.md)

`CPaintDC`

## <a name="requirements"></a>Требования

**Заголовок:** afxwin.h

## <a name="cpaintdccpaintdc"></a><a name="cpaintdc"></a> Кпаинтдк:: Кпаинтдк

Конструирует `CPaintDC` объект, готовит окно приложения для рисования и сохраняет структуру [PAINTSTRUCT](/windows/win32/api/winuser/ns-winuser-paintstruct) в переменной-члене [m_ps](#m_ps) .

```
explicit CPaintDC(CWnd* pWnd);
```

### <a name="parameters"></a>Параметры

*Приводится*<br/>
Указывает на `CWnd` объект, `CPaintDC` которому принадлежит объект.

### <a name="remarks"></a>Комментарии

Исключение (типа `CResourceException` ) выдается при сбое вызова Windows [GetDC](/windows/win32/api/winuser/nf-winuser-getdc) . Контекст устройства может быть недоступен, если в Windows уже выделены все доступные контексты устройств. Приложение будет конкурировать за пять распространенных контекстов вывода, доступных в любой момент в Windows.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCDocView#97](../../mfc/codesnippet/cpp/cpaintdc-class_1.cpp)]

## <a name="cpaintdcm_hwnd"></a><a name="m_hwnd"></a> Кпаинтдк:: m_hWnd

, `HWND` К которому `CPaintDC` присоединен этот объект.

```
HWND m_hWnd;
```

### <a name="remarks"></a>Комментарии

*m_hWnd* является защищенной переменной типа HWND.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCDocView#98](../../mfc/codesnippet/cpp/cpaintdc-class_2.cpp)]

## <a name="cpaintdcm_ps"></a><a name="m_ps"></a> Кпаинтдк:: m_ps

`m_ps` — Это открытая переменная-член типа [PAINTSTRUCT](/windows/win32/api/winuser/ns-winuser-paintstruct).

```
PAINTSTRUCT m_ps;
```

### <a name="remarks"></a>Комментарии

Это объект `PAINTSTRUCT` , который передается и заполняется методом [CWnd:: бегинпаинт](../../mfc/reference/cwnd-class.md#beginpaint).

`PAINTSTRUCT`Содержит сведения, используемые приложением для заполнения клиентской области окна, связанного с `CPaintDC` объектом.

Обратите внимание, что доступ к обработчику контекста устройства можно получить с помощью `PAINTSTRUCT` . Тем не менее можно получить доступ к этому обработчику напрямую через `m_hDC` переменную-член, которая `CPaintDC` наследуется от CDC.

### <a name="example"></a>Пример

  См. пример для [кпаинтдк:: m_hWnd](#m_hwnd).

## <a name="see-also"></a>См. также раздел

[Образец MDI-формы MFC](../../overview/visual-cpp-samples.md)<br/>
[CDC, класс](../../mfc/reference/cdc-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)
