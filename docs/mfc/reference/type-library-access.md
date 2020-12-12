---
description: 'Дополнительные сведения: доступ к библиотеке типов'
title: Доступ к библиотеке типов
ms.date: 11/04/2016
helpviewer_keywords:
- type libraries [MFC], accessing
ms.assetid: a03fa7f0-86c2-4119-bf81-202916fb74b3
ms.openlocfilehash: c855f82914e540ab13f4bc20581c041633b5bc0d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97218658"
---
# <a name="type-library-access"></a>Доступ к библиотеке типов

Библиотеки типов предоставляют интерфейсы элемента управления OLE другим приложениям, поддерживающим технологию OLE. Каждый элемент управления OLE должен иметь библиотеку типов, если требуется предоставить один или несколько интерфейсов.

Следующие макросы позволяют элементу управления OLE предоставлять доступ к собственной библиотеке типов:

### <a name="type-library-access"></a>Доступ к библиотеке типов

|Имя|Описание|
|-|-|
|[DECLARE_OLETYPELIB](#declare_oletypelib)|Объявляет функцию- `GetTypeLib` член элемента управления OLE (должна использоваться в объявлении класса).|
|[IMPLEMENT_OLETYPELIB](#implement_oletypelib)|Реализует `GetTypeLib` функцию-член элемента управления OLE (должна использоваться в реализации класса).|

## <a name="declare_oletypelib"></a><a name="declare_oletypelib"></a> DECLARE_OLETYPELIB

Объявляет `GetTypeLib` функцию члена класса Control.

```
DECLARE_OLETYPELIB(class_name)
```

### <a name="parameters"></a>Параметры

*class_name*<br/>
Имя класса элемента управления, связанного с библиотекой типов.

### <a name="remarks"></a>Комментарии

Используйте этот макрос в файле заголовка класса элемента управления.

### <a name="requirements"></a>Требования

**Заголовок:** afxdisp.h

## <a name="implement_oletypelib"></a><a name="implement_oletypelib"></a> IMPLEMENT_OLETYPELIB

Реализует `GetTypeLib` функцию элемента элемента управления.

```
IMPLEMENT_OLETYPELIB(class_name, tlid, wVerMajor,  wVerMinor)
```

### <a name="parameters"></a>Параметры

*class_name*<br/>
Имя класса элемента управления, связанного с библиотекой типов.

*тлид*<br/>
ИДЕНТИФИКАЦИОНный номер библиотеки типов.

*ввермажор*<br/>
Основной номер версии библиотеки типов.

*вверминор*<br/>
Дополнительный номер версии библиотеки типов.

### <a name="remarks"></a>Комментарии

Этот макрос должен присутствовать в файле реализации для любого класса элементов управления, использующего макрос DECLARE_OLETYPELIB.

### <a name="requirements"></a>Требования

**Заголовок:** afxdisp.h

## <a name="see-also"></a>См. также раздел

[Макросы и глобальные объекты](../../mfc/reference/mfc-macros-and-globals.md)
