---
description: 'Дополнительные сведения о: Microsoft:: WRL:: оболочки:: метод HandleTraits Namespace'
title: Пространство имен Microsoft::WRL::Wrappers::HandleTraits
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits
helpviewer_keywords:
- HandleTraits namespace
ms.assetid: 2fb5c6d1-bfc2-4e09-91eb-31705064ffb3
ms.openlocfilehash: 4bbc970a6d3445e8acda752be1a2030ee99759a8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97178060"
---
# <a name="microsoftwrlwrappershandletraits-namespace"></a>Пространство имен Microsoft::WRL::Wrappers::HandleTraits

Описывает характеристики общих типов ресурсов на основе маркеров.

## <a name="syntax"></a>Синтаксис

```cpp
namespace Microsoft::WRL::Wrappers::HandleTraits;
```

## <a name="members"></a>Члены

### <a name="structures"></a>Структуры

|Имя|Описание|
|----------|-----------------|
|[CriticalSectionTraits - структура](criticalsectiontraits-structure.md)|Специализирует `CriticalSection` объект для поддержки недопустимого критического раздела или функции для освобождения критического раздела.|
|[EventTraits - структура](eventtraits-structure.md)|Определяет характеристики `Event` обработчика класса.|
|[FileHandleTraits - структура](filehandletraits-structure.md)|Определяет характеристики маркера файла.|
|[HANDLENullTraits - структура](handlenulltraits-structure.md)|Определяет общие характеристики неинициализированного маркера.|
|[HANDLETraits - структура](handletraits-structure.md)|Определяет общие характеристики дескриптора.|
|[MutexTraits - структура](mutextraits-structure.md)|Определяет общие характеристики класса [мьютекса](mutex-class.md) .|
|[SemaphoreTraits - структура](semaphoretraits-structure.md)|Определяет общие характеристики объекта семафора.|
|[SRWLockExclusiveTraits - структура](srwlockexclusivetraits-structure.md)|Описывает общие характеристики `SRWLock` класса в режиме монопольной блокировки.|
|[SRWLockSharedTraits - структура](srwlocksharedtraits-structure.md)|Описывает общие характеристики `SRWLock` класса в режиме общей блокировки.|

## <a name="requirements"></a>Требования

**Заголовок:** кореврапперс. h

**Пространство имен:** Программы Microsoft:: WRL:: оболочки

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL:: оберток](microsoft-wrl-wrappers-namespace.md)
