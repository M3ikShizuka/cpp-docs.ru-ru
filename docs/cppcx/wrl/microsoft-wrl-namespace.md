---
description: 'Дополнительные сведения о: Microsoft:: WRL Namespace'
title: Пространство имен Microsoft::WRL
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL
- module/Microsoft::WRL
- async/Microsoft::WRL
- internal/Microsoft::WRL
- event/Microsoft::WRL
- ftm/Microsoft::WRL
- client/Microsoft::WRL
- corewrappers/Microsoft::WRL
helpviewer_keywords:
- WRL namespace
ms.assetid: 01118a8f-f564-4859-b87e-9444848585a1
ms.openlocfilehash: fdf7f0fbdca5cd5d95772052dd5dfb5018cabb18
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335534"
---
# <a name="microsoftwrl-namespace"></a>Пространство имен Microsoft::WRL

Определяет фундаментальные типы, составляющие библиотеку шаблонов C++ среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```cpp
namespace Microsoft::WRL;
```

## <a name="members"></a>Члены

### <a name="typedefs"></a>Определения типов

|Имя|Описание|
|----------|-----------------|
|`InhibitWeakReferencePolicy`|`RuntimeClassFlags<WinRt | InhibitWeakReference>`|

### <a name="classes"></a>Классы

|name|Описание|
|----------|-----------------|
|[Класс метод ActivationFactory](activationfactory-class.md)|Позволяет одному или нескольким классам быть активированными средой выполнения Windows.|
|[Класс метод asyncbase](asyncbase-class.md)|Реализует асинхронный конечный автомат среды выполнения Windows.|
|[Класс ClassFactory](classfactory-class.md)|Реализует базовую функциональность интерфейса `IClassFactory`.|
|[Класс ComPtr](comptr-class.md)|Создает тип *интеллектуальный указатель* , который представляет интерфейс, определяемый параметром шаблона. ComPtr автоматически поддерживает счетчик ссылок для указателя базового интерфейса и освобождает интерфейс, когда счетчик ссылок становится равен нулю.|
|[Класс метод deferrableeventargs](deferrableeventargs-class.md)|Класс шаблона, используемый для типов аргументов событий для задержек.|
|[EventSource](eventsource-class.md)|Представляет событие. Функции-члены `EventSource` добавляют, удаляют и вызывают обработчики событий.|
|[Класс метод FtmBase](ftmbase-class.md)|Представляет свободнопоточный объект маршаллера.|
|[Класс Module](module-class.md)|Представляет коллекцию связанных объектов.|
|[Класс RuntimeClass](runtimeclass-class.md)|Представляет экземпляр класса, который наследует указанное число интерфейсов и предоставляет указанную среду выполнения Windows, классическую COM-модель и поддержку слабых ссылок.|
|[Класс метод simpleactivationfactory](simpleactivationfactory-class.md)|Предоставляет основной механизм для создания базового класса среды выполнения Windows или классической модели COM.|
|[Класс метод simpleclassfactory](simpleclassfactory-class.md)|Предоставляет основной механизм для создания базового класса.|
|[Класс WeakRef](weakref-class.md)|Представляет собой *слабую ссылку* , которая может использоваться только в среде выполнения Windows, а не в классической модели COM. Слабая ссылка представляет собой объект, который может быть доступен или недоступен.|

### <a name="structures"></a>Структуры

|Имя|Описание|
|----------|-----------------|
|[ChainInterfaces - структура](chaininterfaces-structure.md)|Указывает функции проверки и инициализации, которые могут применяться к набору идентификаторов интерфейсов.|
|[CloakedIid - структура](cloakediid-structure.md)|Указывает на `RuntimeClass` , а также на `Implements` шаблоны, `ChainInterfaces` которые указанный интерфейс недоступен в списке IID.|
|[Implements - структура](implements-structure.md)|Реализует `QueryInterface` и `GetIid` для указанных интерфейсов.|
|[MixIn - структура](mixin-structure.md)|Гарантирует, что класс среды выполнения является производным от интерфейсов среды выполнения Windows, если таковые имеются, а затем от интерфейсов классической модели COM.|
|[RuntimeClassFlags - структура](runtimeclassflags-structure.md)|Содержит тип для экземпляра [RuntimeClass](runtimeclass-class.md).|

### <a name="enumerations"></a>Перечисления

|Имя|Описание|
|----------|-----------------|
|[AsyncResultType - перечисление](asyncresulttype-enumeration.md)|Указывает тип результата, возвращаемого `GetResults()` методом.|
|[ModuleType - перечисление](moduletype-enumeration.md)|Указывает, должен ли модуль поддерживать внутрипроцессный или внепроцессный сервер.|
|[RuntimeClassType - перечисление](runtimeclasstype-enumeration.md)|Указывает поддерживаемый тип экземпляра [RuntimeClass](runtimeclass-class.md) .|

### <a name="functions"></a>Функции

|Имя|Описание|
|----------|-----------------|
|[Функция AsWeak](asweak-function.md)|Извлекает слабую ссылку на определенный экземпляр.|
|[Функция обратного вызова (WRL)](callback-function-wrl.md)|Создает объект, функция-член которого является методом обратного вызова.|
|[Функция Креатеактиватионфактори](createactivationfactory-function.md)|Создает фабрику, производящую экземпляры указанного класса, которые могут быть активированы средой выполнения Windows.|
|[Функция Createclassfactory-](createclassfactory-function.md)|Создает фабрику, которая создает экземпляры указанного класса.|
|[Make, функция](make-function.md)|Инициализирует указанный класс среда выполнения Windows.|

## <a name="requirements"></a>Требования

**Заголовок:** Async. h, Client. h, кореврапперс. h, Event. h, FTM. h, реализует. h, internal. h, Module. h

**Пространство имен:** Microsoft::WRL

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL:: оберток](microsoft-wrl-wrappers-namespace.md)
