---
description: 'Дополнительные сведения: &lt; выполнение&gt;'
title: '&lt;InstancePersistenceCommand&gt;'
ms.date: 01/15/2021
f1_keywords:
- <execution>
- execution/std::execution
- std::execution
helpviewer_keywords:
- execution header
ms.openlocfilehash: 2ffba3ad8620092676588c2a67e36cf8956413ba
ms.sourcegitcommit: 3d9cfde85df33002e3b3d7f3509ff6a8dc4c0a21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "98667484"
---
# `<execution>`

Описывает политики выполнения для параллельных алгоритмов.

## <a name="syntax"></a>Синтаксис

```cpp
namespace std {
    template<class T> inline constexpr bool is_execution_policy_v = is_execution_policy<T>::value;
}
namespace std::execution {
    inline constexpr sequenced_policy seq { unspecified };
    inline constexpr parallel_policy par { unspecified };
    inline constexpr parallel_unsequenced_policy par_unseq { unspecified };
}
```

### <a name="classes-and-structs"></a>Классы и структуры

|Имя|Описание|
|-|-|
|[`is_execution_policy` Struct](is-execution-policy-struct.md)|Обнаруживает политики выполнения для исключения определенных сигнатур функций из неоднозначного участия в разрешении перегрузки.|
|[`parallel_policy` См](parallel-policy-class.md)|Используется в качестве уникального типа для устранения неоднозначности при перегрузке параллельного алгоритма. Указывает, что выполнение параллельного алгоритма может быть параллельным.|
|[`parallel_unsequenced_policy` См](parallel-unsequenced-policy-class.md)|Используется в качестве уникального типа для устранения неоднозначности при перегрузке параллельного алгоритма. Указывает, что выполнение параллельного алгоритма может быть параллельно и векторным.|
|[`sequenced_policy` См](sequenced-policy-class.md)|Используется в качестве уникального типа для устранения неоднозначности при перегрузке параллельного алгоритма. Указывает, что выполнение параллельного алгоритма может не быть параллельным.|

## <a name="requirements"></a>Требования

**Заголовок:**\<execution>

**Пространство имен:** stdext

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](cpp-standard-library-header-files.md)\
[Безопасность потоков в стандартной библиотеке C++](thread-safety-in-the-cpp-standard-library.md)\
[Справочник по стандартной библиотеке C++](cpp-standard-library-reference.md)
