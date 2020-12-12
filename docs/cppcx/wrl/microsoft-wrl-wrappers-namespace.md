---
description: 'Дополнительные сведения о: Microsoft:: WRL:: оболочки Namespace'
title: Пространство имен Microsoft::WRL::Wrappers
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers
helpviewer_keywords:
- Wrappers namespace
ms.assetid: 36ac38c7-1fc3-42da-a879-5c68661dc9e1
ms.openlocfilehash: 603fa14b0e43f481b1afe56d98e355d328f284fe
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97209403"
---
# <a name="microsoftwrlwrappers-namespace"></a>Пространство имен Microsoft::WRL::Wrappers

Определяет оболочки типа "Получение ресурса есть инициализация" (RAII), которые упрощают управление временем существования объектов, строк и дескрипторов.

## <a name="syntax"></a>Синтаксис

```cpp
namespace Microsoft::WRL::Wrappers;
```

## <a name="members"></a>Члены

### <a name="typedefs"></a>Определения типов

|Имя|Описание|
|----------|-----------------|
|`FileHandle`|`HandleT<HandleTraits::FileHandleTraits>`|

### <a name="classes"></a>Классы

|name|Описание|
|----------|-----------------|
|[Класс CriticalSection](criticalsection-class.md)|Представляет объект критической секции.|
|[Класс событий (WRL)](event-class-wrl.md)|Представляет событие.|
|[Класс класса Handle](handlet-class.md)|Представляет дескриптор объекта.|
|[Класс HString](hstring-class.md)|Обеспечивает поддержку манипуляций с дескрипторами HSTRING.|
|[Класс HStringReference](hstringreference-class.md)|Представляет HSTRING, созданный из существующей строки.|
|[Класс Mutex](mutex-class.md)|Представляет объект синхронизации, который исключительно управляет общим ресурсом.|
|[Класс RoInitializeWrapper](roinitializewrapper-class.md)|Инициализирует среда выполнения Windows.|
|[Класс семафора](semaphore-class.md)|Представляет объект синхронизации, который управляет общим ресурсом и поддерживает ограниченное число пользователей.|
|[Класс SRWLock](srwlock-class.md)|Представляет тонкую блокировку чтения и записи.|

## <a name="requirements"></a>Требования

**Заголовок:** кореврапперс. h

**Пространство имен:** Программы Microsoft:: WRL:: оболочки

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL](microsoft-wrl-namespace.md)
