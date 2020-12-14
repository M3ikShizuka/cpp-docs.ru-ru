---
description: 'Дополнительные сведения о: &lt; typeindex&gt;'
title: '&lt;typeindex&gt;'
ms.date: 11/04/2016
f1_keywords:
- <typeindex>
ms.assetid: a9551137-f74b-4f02-af64-ff00214cea1f
ms.openlocfilehash: 0f5aee958aee01bcccc87145087001f093ab6749
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97226445"
---
# <a name="lttypeindexgt"></a>&lt;typeindex&gt;

Включите стандартный заголовок \<typeindex> для определения класса и функции, поддерживающей индексирование объектов класса [type_info](../cpp/type-info-class.md).

## <a name="syntax"></a>Синтаксис

```cpp
#include <typeindex>
```

## <a name="remarks"></a>Remarks

[Структура hash](../standard-library/hash-structure.md) определяет `hash function` для сопоставления значений типа [type_index](../standard-library/type-index-class.md) распределению значений индекса.

Класс `type_index` оборачивает указатель в объект `type_info` для индексирования.

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)\
[Справочник по стандартной библиотеке C++](../standard-library/cpp-standard-library-reference.md)
