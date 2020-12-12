---
description: 'Дополнительные сведения о классе Module:: GenericReleaseNotifier'
title: Класс Module::GenericReleaseNotifier
ms.date: 09/17/2018
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Module::GenericReleaseNotifier
- module/Microsoft::WRL::Module::GenericReleaseNotifier::callback_
- module/Microsoft::WRL::Module::GenericReleaseNotifier::GenericReleaseNotifier
- module/Microsoft::WRL::Module::GenericReleaseNotifier::Invoke
helpviewer_keywords:
- Microsoft::WRL::Module::GenericReleaseNotifier class
- Microsoft::WRL::Module::GenericReleaseNotifier::callback_ data member
- Microsoft::WRL::Module::GenericReleaseNotifier::GenericReleaseNotifier, constructor
- Microsoft::WRL::Module::GenericReleaseNotifier::Invoke method
ms.assetid: 244a8fbe-f89b-409b-aa65-db3e37f9b125
ms.openlocfilehash: dd82da7c1b6b9a77c68b6d451bfa6dac31f51180
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97186380"
---
# <a name="modulegenericreleasenotifier-class"></a>Класс Module::GenericReleaseNotifier

Вызывает обработчик событий при освобождении последнего объекта в текущем модуле. Обработчик событий задается лямбда-выражением, функтором или указателем на функцию.

## <a name="syntax"></a>Синтаксис

```cpp
template<typename T>
class GenericReleaseNotifier : public ReleaseNotifier;
```

### <a name="parameters"></a>Параметры

*T*<br/>
Тип данных-члена, который содержит расположение обработчика событий.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

name                                                                                                     | Описание
-------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------
[Модуль:: GenericReleaseNotifier:: GenericReleaseNotifier](#genericreleasenotifier-genericreleasenotifier) | Инициализирует новый экземпляр класса `Module::GenericReleaseNotifier`.

### <a name="public-methods"></a>Открытые методы

name                                                                     | Описание
------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------
[Модуль:: GenericReleaseNotifier:: Invoke](#genericreleasenotifier-invoke) | Вызывает обработчик событий, связанный с текущим `Module::GenericReleaseNotifier` объектом.

### <a name="protected-data-members"></a>Защищенные члены данных

Имя                                                                          | Описание
----------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------
[Модуль:: GenericReleaseNotifier:: callback_](#genericreleasenotifier-callback) | Содержит лямбда-, функтор или указатель на функцию-обработчик событий, связанный с текущим `Module::GenericReleaseNotifier` объектом.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`ReleaseNotifier`

`GenericReleaseNotifier`

## <a name="requirements"></a>Требования

**Заголовок:** Module. h

**Пространство имен:** Microsoft::WRL

## <a name="modulegenericreleasenotifiercallback_"></a><a name="genericreleasenotifier-callback"></a> Модуль:: GenericReleaseNotifier:: callback_

Содержит лямбда-, функтор или указатель на функцию-обработчик событий, связанный с текущим `Module::GenericReleaseNotifier` объектом.

```cpp
T callback_;
```

## <a name="modulegenericreleasenotifiergenericreleasenotifier"></a><a name="genericreleasenotifier-genericreleasenotifier"></a> Модуль:: GenericReleaseNotifier:: GenericReleaseNotifier

Инициализирует новый экземпляр класса `Module::GenericReleaseNotifier`.

```cpp
GenericReleaseNotifier(
   T callback,
   bool release
) throw() : ReleaseNotifier(release), callback_(callback);
```

### <a name="parameters"></a>Параметры

*обратный вызов*<br/>
Обработчик событий лямбда-, функтор или указателя на функцию, который можно вызвать с помощью оператора-функции в круглых скобках ( `()` ).

*отпускании*<br/>
Укажите, **`true`** чтобы разрешить вызов базового метода [модуля:: ReleaseNotifier:: Release ()](module-releasenotifier-class.md#releasenotifier-release) ; в противном случае укажите **`false`** .

## <a name="modulegenericreleasenotifierinvoke"></a><a name="genericreleasenotifier-invoke"></a> Модуль:: GenericReleaseNotifier:: Invoke

Вызывает обработчик событий, связанный с текущим `Module::GenericReleaseNotifier` объектом.

```cpp
void Invoke();
```
