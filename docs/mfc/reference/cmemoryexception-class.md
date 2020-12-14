---
description: 'Дополнительные сведения о: CMemoryException Class'
title: Класс CMemoryException
ms.date: 11/04/2016
f1_keywords:
- CMemoryException
- AFX/CMemoryException
- AFX/CMemoryException::CMemoryException
helpviewer_keywords:
- CMemoryException [MFC], CMemoryException
ms.assetid: 9af0ed57-d12a-45ca-82b5-c910a60f7edf
ms.openlocfilehash: 694629d65c8b4cffc351873d5da3d8ed3c34cf8e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336652"
---
# <a name="cmemoryexception-class"></a>Класс CMemoryException

Представляет условие исключения вне памяти.

## <a name="syntax"></a>Синтаксис

```
class CMemoryException : public CSimpleException
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CMemoryException:: CMemoryException](#cmemoryexception)|Формирует объект `CMemoryException`.|

## <a name="remarks"></a>Комментарии

Дальнейшая квалификация не требуется или невозможна. Исключения памяти автоматически создаются **`new`** . При написании собственных функций для работы с памятью с помощью, например, `malloc` вы несете ответственность за создание исключений памяти.

Дополнительные сведения о см `CMemoryException` . в статье [обработка исключений (MFC)](../../mfc/exception-handling-in-mfc.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CException](../../mfc/reference/cexception-class.md)

[CSimpleException](../../mfc/reference/csimpleexception-class.md)

`CMemoryException`

## <a name="requirements"></a>Требования

**Заголовок:** AFX. h

## <a name="cmemoryexceptioncmemoryexception"></a><a name="cmemoryexception"></a> CMemoryException:: CMemoryException

Формирует объект `CMemoryException`.

```
CMemoryException();
```

### <a name="remarks"></a>Комментарии

Не используйте этот конструктор напрямую, а вызовите глобальную функцию [афкссровмеморексцептион](exception-processing.md#afxthrowmemoryexception). Эта глобальная функция может быть выполнена в случае нехватки памяти, так как она конструирует объект исключения в ранее выделенной памяти. Дополнительные сведения об обработке исключений см. в статье [исключения](../exception-handling-in-mfc.md).

## <a name="see-also"></a>См. также раздел

[Класс CException](cexception-class.md)<br/>
[Иерархическая диаграмма](../hierarchy-chart.md)
