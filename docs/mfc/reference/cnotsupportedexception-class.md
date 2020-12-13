---
description: 'Дополнительные сведения о: Кнотсуппортедексцептион Class'
title: Класс Кнотсуппортедексцептион
ms.date: 11/04/2016
f1_keywords:
- CNotSupportedException
- AFX/CNotSupportedException
- AFX/CNotSupportedException::CNotSupportedException
helpviewer_keywords:
- CNotSupportedException [MFC], CNotSupportedException
ms.assetid: e517391b-eb94-4c39-ae32-87b45bf7d624
ms.openlocfilehash: 61bf729753897e1d30c5a12bc371489ba6f2d64f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331483"
---
# <a name="cnotsupportedexception-class"></a>Класс Кнотсуппортедексцептион

Представляет исключение, являющееся результатом запроса неподдерживаемой возможности.

## <a name="syntax"></a>Синтаксис

```
class CNotSupportedException : public CSimpleException
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кнотсуппортедексцептион:: Кнотсуппортедексцептион](#cnotsupportedexception)|Формирует объект `CNotSupportedException`.|

## <a name="remarks"></a>Комментарии

Дальнейшая квалификация не требуется или невозможна.

Дополнительные сведения об использовании см `CNotSupportedException` . в статье [обработка исключений (MFC)](../../mfc/exception-handling-in-mfc.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CException](../../mfc/reference/cexception-class.md)

[CSimpleException](../../mfc/reference/csimpleexception-class.md)

`CNotSupportedException`

## <a name="requirements"></a>Требования

**Заголовок:** AFX. h

## <a name="cnotsupportedexceptioncnotsupportedexception"></a><a name="cnotsupportedexception"></a> Кнотсуппортедексцептион:: Кнотсуппортедексцептион

Формирует объект `CNotSupportedException`.

```
CNotSupportedException();
```

### <a name="remarks"></a>Комментарии

Не используйте этот конструктор напрямую, а вызовите глобальную функцию [афкссровнотсуппортедексцептион](exception-processing.md#afxthrownotsupportedexception). Дополнительные сведения об обработке исключений см. в статье [обработка исключений в MFC](../exception-handling-in-mfc.md).

## <a name="see-also"></a>См. также раздел

[Класс CException](cexception-class.md)<br/>
[Иерархическая диаграмма](../hierarchy-chart.md)
