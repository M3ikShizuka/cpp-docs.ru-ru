---
description: 'Дополнительные сведения: &lt; выполнение&gt;'
title: '&lt;InstancePersistenceCommand&gt;'
ms.date: 04/18/2019
f1_keywords:
- <execution>
helpviewer_keywords:
- execution header
ms.openlocfilehash: 7603bc6a78671482f691f15f83f51439a5002870
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98126576"
---
# <a name="ltexecutiongt"></a>&lt;InstancePersistenceCommand&gt;

Описывает политики выполнения для параллельных алгоритмов.

## <a name="syntax"></a>Синтаксис

```
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
|[Структура is_execution_policy](is-execution-policy-struct.md)|Обнаруживает политики выполнения в целях исключения сигнатур функций из неоднозначного участия в разрешении перегрузки.|
|[Класс parallel_policy](parallel-policy-class.md)|Используется в качестве уникального типа для устранения неоднозначности при перегрузке параллельного алгоритма и указывает, что выполнение параллельного алгоритма может быть параллельным.|
|[Класс parallel_unsequenced_policy](parallel-unsequenced-policy-class.md)|Используется в качестве уникального типа для устранения неоднозначности при перегрузке параллельного алгоритма и указывает, что выполнение параллельного алгоритма может быть параллельным и векторным.|
|[Класс sequenced_policy](sequenced-policy-class.md)|Используется в качестве уникального типа для устранения неоднозначности при перегрузке параллельного алгоритма и требует, чтобы выполнение параллельного алгоритма не было параллельным.|

## <a name="requirements"></a>Требования

**Заголовок:**\<execution>

**Пространство имен:** stdext

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](cpp-standard-library-header-files.md)\
[Безопасность потоков в стандартной библиотеке C++](thread-safety-in-the-cpp-standard-library.md)\
[Справочник по стандартной библиотеке C++](cpp-standard-library-reference.md)
