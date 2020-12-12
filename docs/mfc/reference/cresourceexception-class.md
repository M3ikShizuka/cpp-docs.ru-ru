---
description: 'Дополнительные сведения о: Кресаурцеексцептион Class'
title: Класс Кресаурцеексцептион
ms.date: 11/04/2016
f1_keywords:
- CResourceException
- AFXWIN/CResourceException
- AFXWIN/CResourceException::CResourceException
helpviewer_keywords:
- CResourceException [MFC], CResourceException
ms.assetid: af6ae043-d124-4bfd-b35e-7bb0db67d289
ms.openlocfilehash: c76635ae2cfa6c55bf54da7e73f6afbb44506fee
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97264873"
---
# <a name="cresourceexception-class"></a>Класс Кресаурцеексцептион

Генерируется, когда Windows не может найти или выбрать запрошенный ресурс.

## <a name="syntax"></a>Синтаксис

```
class CResourceException : public CSimpleException
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кресаурцеексцептион:: Кресаурцеексцептион](#cresourceexception)|Формирует объект `CResourceException`.|

## <a name="remarks"></a>Комментарии

Дальнейшая квалификация не требуется или невозможна.

Дополнительные сведения об использовании см `CResourceException` . в статье [обработка исключений (MFC)](../../mfc/exception-handling-in-mfc.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CException](../../mfc/reference/cexception-class.md)

[CSimpleException](../../mfc/reference/csimpleexception-class.md)

`CResourceException`

## <a name="requirements"></a>Требования

**Заголовок:** afxwin.h

## <a name="cresourceexceptioncresourceexception"></a><a name="cresourceexception"></a> Кресаурцеексцептион:: Кресаурцеексцептион

Формирует объект `CResourceException`.

```
CResourceException();
```

### <a name="remarks"></a>Комментарии

Не используйте этот конструктор напрямую, а вызовите глобальную функцию [афкссровресаурцеексцептион](exception-processing.md#afxthrowresourceexception). Дополнительные сведения об исключениях см. в статье [обработка исключений в MFC](../exception-handling-in-mfc.md).

## <a name="see-also"></a>См. также раздел

[Класс CException](cexception-class.md)<br/>
[Иерархическая диаграмма](../hierarchy-chart.md)
