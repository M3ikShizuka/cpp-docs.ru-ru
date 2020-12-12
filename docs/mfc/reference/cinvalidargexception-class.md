---
description: 'Дополнительные сведения о: Цинвалидаржексцептион Class'
title: Класс Цинвалидаржексцептион
ms.date: 11/04/2016
f1_keywords:
- CInvalidArgException
- AFX/CInvalidArgException
- AFX/CInvalidArgException::CInvalidArgException
helpviewer_keywords:
- CInvalidArgException [MFC], CInvalidArgException
ms.assetid: e43d7c67-1157-47f8-817a-804083e8186e
ms.openlocfilehash: f68642747a81d1c45a8246f4f25abfb8b79c81d8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97202799"
---
# <a name="cinvalidargexception-class"></a>Класс Цинвалидаржексцептион

Этот класс представляет условие исключения, связанного с недопустимым аргументом.

## <a name="syntax"></a>Синтаксис

```
class CInvalidArgException : public CSimpleException
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Цинвалидаржексцептион:: Цинвалидаржексцептион](#cinvalidargexception)|Конструктор.|

## <a name="remarks"></a>Комментарии

`CInvalidArgException`Объект представляет условие исключения недопустимого аргумента.

Дополнительные сведения об обработке исключений см. в разделе [Класс CException](../../mfc/reference/cexception-class.md) и [обработка исключений (MFC)](../../mfc/exception-handling-in-mfc.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CException](../../mfc/reference/cexception-class.md)

[CSimpleException](../../mfc/reference/csimpleexception-class.md)

`CInvalidArgException`

## <a name="requirements"></a>Требования

**Заголовок:** AFX. h

## <a name="cinvalidargexceptioncinvalidargexception"></a><a name="cinvalidargexception"></a> Цинвалидаржексцептион:: Цинвалидаржексцептион

Конструктор.

```
CInvalidArgException();
```

### <a name="remarks"></a>Комментарии

Не используйте этот конструктор напрямую; Вызовите глобальную функцию **афкссровинвалидаржексцептион**.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Ксимпликсцептион](../../mfc/reference/csimpleexception-class.md)
