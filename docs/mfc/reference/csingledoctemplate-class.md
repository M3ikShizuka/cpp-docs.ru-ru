---
description: 'Дополнительные сведения о: Ксингледоктемплате Class'
title: Класс Ксингледоктемплате
ms.date: 11/04/2016
f1_keywords:
- CSingleDocTemplate
- AFXWIN/CSingleDocTemplate
- AFXWIN/CSingleDocTemplate::CSingleDocTemplate
helpviewer_keywords:
- CSingleDocTemplate [MFC], CSingleDocTemplate
ms.assetid: 4f3a8212-81ee-48a0-ad22-e0ed7c36a391
ms.openlocfilehash: 611cada1c90fa776bafb78f0856658cd1bd0a8e4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97264626"
---
# <a name="csingledoctemplate-class"></a>Класс Ксингледоктемплате

Определяет шаблон документа, реализующий интерфейс одного документа (SDI).

## <a name="syntax"></a>Синтаксис

```
class CSingleDocTemplate : public CDocTemplate
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ксингледоктемплате:: Ксингледоктемплате](#csingledoctemplate)|Формирует объект `CSingleDocTemplate`.|

## <a name="remarks"></a>Комментарии

Приложение SDI использует главное окно фрейма для вывода документа. в каждый момент времени может быть открыт только один документ.

Шаблон документа определяет связь между тремя типами классов:

- Класс документа, производный от `CDocument` .

- Класс представления, который отображает данные из указанного выше класса документа. Этот класс можно наследовать от `CView` ,, `CScrollView` `CFormView` или `CEditView` . (Можно также использовать `CEditView` напрямую.)

- Класс окна фрейма, который содержит представление. Для шаблона документа SDI этот класс можно наследовать от `CFrameWnd` ; если не требуется настраивать поведение главного окна фрейма, можно использовать `CFrameWnd` напрямую, не создавая собственный класс.

Приложение SDI обычно поддерживает один тип документов, поэтому он содержит только один `CSingleDocTemplate` объект. В каждый момент времени может быть открыт только один документ.

Вам не нужно вызывать никакие функции члена, `CSingleDocTemplate` кроме конструктора. Платформа обрабатывает `CSingleDocTemplate` объекты внутренним образом.

Дополнительные сведения об использовании см `CSingleDocTemplate` . в разделе [шаблоны документов и процесс создания документа/представления](../../mfc/document-templates-and-the-document-view-creation-process.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CDocTemplate](../../mfc/reference/cdoctemplate-class.md)

`CSingleDocTemplate`

## <a name="requirements"></a>Требования

**Заголовок:** afxwin.h

## <a name="csingledoctemplatecsingledoctemplate"></a><a name="csingledoctemplate"></a> Ксингледоктемплате:: Ксингледоктемплате

Формирует объект `CSingleDocTemplate`.

```
CSingleDocTemplate(
    UINT nIDResource,
    CRuntimeClass* pDocClass,
    CRuntimeClass* pFrameClass,
    CRuntimeClass* pViewClass);
```

### <a name="parameters"></a>Параметры

*нидресаурце*<br/>
Указывает идентификатор ресурсов, используемых с типом документа. Это может быть меню, значок, таблица сочетаний клавиш и строковые ресурсы.

Строковый ресурс состоит из до семи подстрок, разделенных символом "\n" (символ "\n" требуется в качестве заполнителя, если подстрока не включена; Однако завершающие символы "\n" не требуются); эти подстроки описывают тип документа. Дополнительные сведения о подстроках см. в разделе [CDocTemplate:: жетдокстринг](../../mfc/reference/cdoctemplate-class.md#getdocstring). Этот строковый ресурс находится в файле ресурсов приложения. Пример:

```RC
// MYCALC.RC
STRINGTABLE PRELOAD DISCARDABLE
BEGIN
  IDR_MAINFRAME "MyCalc Windows Application\nSheet\nWorksheet\n Worksheets (*.myc)\n.myc\nMyCalcSheet\n MyCalc Worksheet"
END
```

Эту строку можно изменить с помощью редактора строк. вся строка отображается в виде одной записи в редакторе строк, а не в виде семи отдельных записей.

Дополнительные сведения об этих типах ресурсов см. в разделе [Редактор строк](../../windows/string-editor.md).

*пдоккласс*<br/>
Указывает на `CRuntimeClass` объект класса Document. Этот класс является производным от класса, `CDocument` который определяется для представления документов.

*пфрамекласс*<br/>
Указывает на `CRuntimeClass` объект класса фрейм окна. Этот класс может быть `CFrameWnd` производным от класса или, `CFrameWnd` Если требуется поведение по умолчанию для основного окна фрейма.

*пвиевкласс*<br/>
Указывает на `CRuntimeClass` объект класса представления. Этот класс является производным от класса, `CView` который определяется для вывода документов.

### <a name="remarks"></a>Комментарии

Динамическое выделение `CSingleDocTemplate` объекта и передача его `CWinApp::AddDocTemplate` из функции- `InitInstance` члена класса приложения.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCDocViewSDI#13](../../mfc/codesnippet/cpp/csingledoctemplate-class_1.cpp)]

[!code-cpp[NVC_MFCDocViewSDI#14](../../mfc/codesnippet/cpp/csingledoctemplate-class_2.cpp)]

## <a name="see-also"></a>См. также раздел

[Пример ДОККТУЛ для MFC](../../overview/visual-cpp-samples.md)<br/>
[Класс CDocTemplate](../../mfc/reference/cdoctemplate-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс CDocTemplate](../../mfc/reference/cdoctemplate-class.md)<br/>
[Класс CDocument](../../mfc/reference/cdocument-class.md)<br/>
[Класс CFrameWnd](../../mfc/reference/cframewnd-class.md)<br/>
[Класс Кмултидоктемплате](../../mfc/reference/cmultidoctemplate-class.md)<br/>
[Класс CView](../../mfc/reference/cview-class.md)<br/>
[Класс CWinApp](../../mfc/reference/cwinapp-class.md)
