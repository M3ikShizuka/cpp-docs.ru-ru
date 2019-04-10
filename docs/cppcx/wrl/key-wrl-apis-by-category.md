---
title: Основные API WRL по категориям
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 7367bacf-6b7c-4ecd-a0ce-a662db46fc66
ms.openlocfilehash: f3065323c567c944dab12fc1ebbcbd6bb57127e9
ms.sourcegitcommit: c7f90df497e6261764893f9cc04b5d1f1bf0b64b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2019
ms.locfileid: "59039062"
---
# <a name="key-wrl-apis-by-category"></a>Основные API WRL по категориям

В следующих таблицах перечислены основной классы, структуры, функции и макросы библиотека шаблонов C++ среды выполнения Windows. Конструкции в вспомогательные пространства имен и классы, опущены. Эти списки дополнить документации по API, упорядоченных по степени пространства имен.

## <a name="classes"></a>Классы

|Заголовок|Описание|
|-----------|-----------------|
|[ActivationFactory - класс](activationfactory-class.md)|Позволяет одному или нескольким классам быть активированными средой выполнения Windows.|
|[AsyncBase - класс](asyncbase-class.md)|Реализует асинхронный конечный автомат среды выполнения Windows.|
|[ClassFactory - класс](classfactory-class.md)|Реализует базовую функциональность интерфейса `IClassFactory`.|
|[Класс ComPtr](comptr-class.md)|Создает тип *интеллектуальный указатель* , который представляет интерфейс, определяемый параметром шаблона. ComPtr автоматически поддерживает счетчик ссылок для указателя базового интерфейса и освобождает интерфейс, когда счетчик ссылок становится равен нулю.|
|[Класс Event (библиотека шаблонов C++ среды выполнения Windows)](event-class-wrl.md)|Представляет событие.|
|[EventSource - класс](eventsource-class.md)|Представляет событие. `EventSource` функции-члены, добавлять, удалять и вызывать обработчики событий.|
|[FtmBase - класс](ftmbase-class.md)|Представляет свободнопоточный объект маршаллера.|
|[HandleT - класс](handlet-class.md)|Представляет дескриптор объекта.|
|[Класс HString](hstring-class.md)|Обеспечивает поддержку манипулирования дескрипторами HSTRING.|
|[Класс HStringReference](hstringreference-class.md)|Представляет HSTRING, созданный из существующей строки.|
|[Module - класс](module-class.md)|Представляет коллекцию связанных объектов.|
|[Класс Module::GenericReleaseNotifier](module-genericreleasenotifier-class.md)|Вызывает обработчик событий при освобождении последнего объекта в текущем модуле. Обработчик событий задается лямбда-выражением, функтором или указателем на функцию.|
|[Класс Module::MethodReleaseNotifier](module-methodreleasenotifier-class.md)|Вызывает обработчик событий при освобождении последнего объекта в текущем модуле. Обработчик событий заданного объекта и ее члена указатель на метод.|
|[Класс Module::ReleaseNotifier](module-releasenotifier-class.md)|Вызывает обработчик событий при освобождении последнего объекта в модуле.|
|[Класс RoInitializeWrapper](roinitializewrapper-class.md)|Инициализирует среду выполнения Windows.|
|[Класс RuntimeClass](runtimeclass-class.md)|Представляет экземпляр класса, который наследует указанное число интерфейсов и предоставляет указанную среду выполнения Windows, классическую COM-модель и поддержку слабых ссылок.|
|[SimpleActivationFactory - класс](simpleactivationfactory-class.md)|Предоставляет основной механизм для создания базового класса среды выполнения Windows или классической модели COM.|
|[SimpleClassFactory - класс](simpleclassfactory-class.md)|Предоставляет основной механизм для создания базового класса.|
|[Класс WeakRef](weakref-class.md)|Представляет собой *слабую ссылку* , которая может использоваться только в среде выполнения Windows, а не в классической модели COM. Слабая ссылка представляет собой объект, который может быть доступен или недоступен.|

## <a name="structures"></a>Структуры

|Заголовок|Описание|
|-----------|-----------------|
|[ChainInterfaces - структура](chaininterfaces-structure.md)|Указывает функции проверки и инициализации, которые могут применяться к набору идентификаторов интерфейсов.|
|[CloakedIid - структура](cloakediid-structure.md)|Указывает `RuntimeClass`, `Implements` и `ChainInterfaces` шаблоны, что заданный интерфейс недоступен в списке IID.|
|[Implements - структура](implements-structure.md)|Реализует `QueryInterface` и `GetIid` для указанных интерфейсов.|
|[MixIn - структура](mixin-structure.md)|Гарантирует, что класс среды выполнения является производным от интерфейсов среды выполнения Windows, если таковые имеются, а затем от интерфейсов классической модели COM.|

## <a name="functions"></a>Функции

|Заголовок|Описание|
|-----------|-----------------|
|[ActivateInstance - функция](activateinstance-function.md)|Регистрирует и возвращает экземпляр заданного типа, определенного в идентификатор указанного класса.|
|[AsWeak - функция](asweak-function.md)|Извлекает слабую ссылку на определенный экземпляр.|
|[Функция Callback](callback-function-wrl.md)|Создает объект, функция-член которого является методом обратного вызова.|
|[CreateActivationFactory - функция](createactivationfactory-function.md)|Создает фабрику, производящую экземпляры указанного класса, которые могут быть активированы средой выполнения Windows.|
|[CreateClassFactory - функция](createclassfactory-function.md)|Создает фабрику, которая создает экземпляры указанного класса.|
|[GetActivationFactory - функция](getactivationfactory-function.md)|Извлекает фабрику активации для типа, указанного в параметре шаблона.|
|[Функция Make](make-function.md)|Инициализирует указанный класс среды выполнения Windows.|

## <a name="macros"></a>Макросы

|Заголовок|Описание|
|-----------|-----------------|
|[Макрос ActivatableClass](activatableclass-macros.md)|Заполняет внутренний кэш, содержащий фабрику, можно создать экземпляр указанного класса.|
|[Макрос InspectableClass](inspectableclass-macro.md)|Задает уровень имя и доверия класса среды выполнения.|

## <a name="see-also"></a>См. также

[Библиотека шаблонов C++ среды выполнения Windows (WRL)](windows-runtime-cpp-template-library-wrl.md)