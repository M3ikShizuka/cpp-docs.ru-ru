---
description: 'Дополнительные сведения: no_registry атрибута импорта'
title: no_registry атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- no_registry
helpviewer_keywords:
- no_registry attribute
ms.assetid: d30de4e2-551c-428c-98fd-951330d578d3
ms.openlocfilehash: fa33bf8096a92ec248b0a9d56e39fcc82f433206
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333304"
---
# <a name="no_registry-import-attribute"></a>no_registry атрибут импорта

**no_registry** указывает компилятору не выполнять поиск в реестре библиотек типов, импортированных с помощью `#import` .

## <a name="syntax"></a>Синтаксис

> **no_registry** типов **#import** *-Library*

### <a name="parameters"></a>Параметры

*Библиотека типов*\
Библиотека типов.

## <a name="remarks"></a>Комментарии

Если библиотека типов, на которую указывает ссылка, не найдена в каталогах включения, компиляция завершается сбоем, даже если библиотека типов находится в реестре.  **no_registry** распространяется на другие библиотеки типов, которые неявно импортируются с помощью `auto_search` .

Компилятор не ищет в реестре библиотеки типов, которые указаны по имени файла и передаются непосредственно в `#import` .

Если `auto_search` указан параметр, дополнительные `#import` директивы создаются с помощью параметра **no_registry** начального `#import` . Если начальная `#import` директива была **no_registry**, `auto_search` создается `#import` также **no_registry**.

**no_registry** удобно использовать, если требуется импортировать библиотеки типов с перекрестными ссылками. Компилятор не находит более раннюю версию файла в реестре. **no_registry** также полезно, если библиотека типов не зарегистрирована.

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
