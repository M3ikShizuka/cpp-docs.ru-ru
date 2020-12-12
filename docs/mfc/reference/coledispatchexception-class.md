---
description: 'Дополнительные сведения о: COleDispatchException Class'
title: Класс COleDispatchException
ms.date: 11/04/2016
f1_keywords:
- COleDispatchException
- AFXDISP/COleDispatchException
- AFXDISP/COleDispatchException::m_dwHelpContext
- AFXDISP/COleDispatchException::m_strDescription
- AFXDISP/COleDispatchException::m_strHelpFile
- AFXDISP/COleDispatchException::m_strSource
- AFXDISP/COleDispatchException::m_wCode
helpviewer_keywords:
- COleDispatchException [MFC], m_dwHelpContext
- COleDispatchException [MFC], m_strDescription
- COleDispatchException [MFC], m_strHelpFile
- COleDispatchException [MFC], m_strSource
- COleDispatchException [MFC], m_wCode
ms.assetid: 0e95c8be-e21a-490c-99ec-181c6a9a26d0
ms.openlocfilehash: 39d8c4652f49b721e5f94c05319e5c1adad07269
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97227212"
---
# <a name="coledispatchexception-class"></a>Класс COleDispatchException

Обрабатывает исключения, относящиеся к интерфейсу OLE `IDispatch` и являющиеся ключевой частью OLE-автоматизации.

## <a name="syntax"></a>Синтаксис

```
class COleDispatchException : public CException
```

## <a name="members"></a>Члены

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[COleDispatchException:: m_dwHelpContext](#m_dwhelpcontext)|Контекст справки для ошибки.|
|[COleDispatchException:: m_strDescription](#m_strdescription)|Описание ошибки текстовом.|
|[COleDispatchException:: m_strHelpFile](#m_strhelpfile)|Файл справки для использования с `m_dwHelpContext` .|
|[COleDispatchException:: m_strSource](#m_strsource)|Приложение, создавшее исключение.|
|[COleDispatchException:: m_wCode](#m_wcode)|`IDispatch`код ошибки.|

## <a name="remarks"></a>Комментарии

Как и другие классы исключений, производные от `CException` базового класса, `COleDispatchException` можно использовать с макросами THROW, THROW_LAST, try, CATCH, AND_CATCH и END_CATCH.

Как правило, следует вызывать [афкссроволедиспатчексцептион](exception-processing.md#afxthrowoledispatchexception) для создания и вызова `COleDispatchException` объекта.

Дополнительные сведения об исключениях см. в статьях [обработка исключений (MFC)](../../mfc/exception-handling-in-mfc.md) и [исключения: OLE Exceptions](../../mfc/exceptions-ole-exceptions.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CException](../../mfc/reference/cexception-class.md)

`COleDispatchException`

## <a name="requirements"></a>Требования

**Заголовок:** afxdisp.h

## <a name="coledispatchexceptionm_dwhelpcontext"></a><a name="m_dwhelpcontext"></a> COleDispatchException:: m_dwHelpContext

Определяет контекст справки в справке приложения (. Файл HLP).

```
DWORD m_dwHelpContext;
```

### <a name="remarks"></a>Комментарии

Этот элемент задается функцией [афкссроволедиспатчексцептион](exception-processing.md#afxthrowoledispatchexception) при возникновении исключения.

### <a name="example"></a>Пример

  См. пример для [COleDispatchDriver::CreateDispatch](../../mfc/reference/coledispatchdriver-class.md#createdispatch).

## <a name="coledispatchexceptionm_strdescription"></a><a name="m_strdescription"></a> COleDispatchException:: m_strDescription

Содержит описание ошибки текстовом, например "диск полон".

```
CString m_strDescription;
```

### <a name="remarks"></a>Комментарии

Этот элемент задается функцией [афкссроволедиспатчексцептион](exception-processing.md#afxthrowoledispatchexception) при возникновении исключения.

### <a name="example"></a>Пример

  См. пример для [COleDispatchDriver::CreateDispatch](../../mfc/reference/coledispatchdriver-class.md#createdispatch).

## <a name="coledispatchexceptionm_strhelpfile"></a><a name="m_strhelpfile"></a> COleDispatchException:: m_strHelpFile

Платформа заполняет эту строку именем файла справки приложения.

```
CString m_strHelpFile;
```

## <a name="coledispatchexceptionm_strsource"></a><a name="m_strsource"></a> COleDispatchException:: m_strSource

Платформа заполняет эту строку именем приложения, создавшего исключение.

```
CString m_strSource;
```

### <a name="example"></a>Пример

  См. пример для [COleDispatchDriver::CreateDispatch](../../mfc/reference/coledispatchdriver-class.md#createdispatch).

## <a name="coledispatchexceptionm_wcode"></a><a name="m_wcode"></a> COleDispatchException:: m_wCode

Содержит код ошибки, относящийся к вашему приложению.

```
WORD m_wCode;
```

### <a name="remarks"></a>Комментарии

Этот элемент задается функцией [афкссроволедиспатчексцептион](exception-processing.md#afxthrowoledispatchexception) при возникновении исключения.

## <a name="see-also"></a>См. также раздел

[Пример CALCDRIV в MFC](../../overview/visual-cpp-samples.md)<br/>
[Класс CException](../../mfc/reference/cexception-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс COleDispatchDriver](../../mfc/reference/coledispatchdriver-class.md)<br/>
[Класс COleException](../../mfc/reference/coleexception-class.md)
