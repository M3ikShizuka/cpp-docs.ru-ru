---
description: 'Дополнительные сведения о классе Platform:: ChangedStateException'
title: Класс Platform::ChangedStateException
ms.date: 12/30/2016
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::ChangedStateException
- VCCORLIB/Platform::ChangedStateException::ChangedStateException
helpviewer_keywords:
- Platform::ChangedStateException
ms.assetid: f894beac-9e80-4fac-ac25-89f1dbc0a6a4
ms.openlocfilehash: baabf54cacfc4dd03256b569fb868c402ea98a97
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97284035"
---
# <a name="platformchangedstateexception-class"></a>Класс Platform::ChangedStateException

Создается, если внутреннее состояние объекта было изменено, тем самым делая недействительными результаты метода.

## <a name="syntax"></a>Синтаксис

```cpp
public ref class ChangedStateException : COMException,    IException,    IPrintable,    IEquatable
```

### <a name="remarks"></a>Remarks

Один из примеров ситуаций, когда создается это исключение: метод итератора коллекции или представления коллекции вызван после изменения родительской коллекции, что делает результаты метода недействительными.

Дополнительные сведения см. в описании класса [COMException](../cppcx/platform-comexception-class.md) .

### <a name="requirements"></a>Требования

**Минимальный поддерживаемый клиент:** Windows 8

**Минимальный поддерживаемый сервер:** Windows Server 2012

**Пространство имен:** Platform

**Метаданные:** Platform. winmd

## <a name="see-also"></a>См. также раздел

[Класс Platform:: COMException](../cppcx/platform-comexception-class.md)
