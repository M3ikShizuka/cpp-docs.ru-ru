---
description: 'Дополнительные сведения о: invoke_result классе'
title: Класс invoke_result
ms.date: 02/21/2019
f1_keywords:
- type_traits/std::invoke_result
- type_traits/std::invoke_result_t
- type_traits/std::invoke_result::type
helpviewer_keywords:
- std::invoke_result
- std::invoke_result_t
- std::invoke_result::type
ms.openlocfilehash: 4204ff1b0b8d38eab4b7d8c0de4709b90e12f5d3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97231501"
---
# <a name="invoke_result-class"></a>Класс invoke_result

Определяет тип возвращаемого значения вызываемого типа, который принимает указанные типы аргументов во время компиляции. Добавлено в C++ 17.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Callable, class... Args>
   struct invoke_result<Callable(Args...)>;

// Helper type
template<class Callable, class... Args>
   using invoke_result_t = typename invoke_result<Callable, Args...>::type;
```

### <a name="parameters"></a>Параметры

*Предназначен*\
Вызываемый тип для запроса.

*Args*\
Типы списка аргументов к вызываемому типу для запроса.

## <a name="remarks"></a>Комментарии

Используйте этот шаблон для определения типа результата *вызываемого*(*args*...) во время компиляции, где *вызываемый* объект и все типы в аргументах *args* являются полным типом, массивом неизвестной привязки или, возможно, с указанием ОПС **`void`** . `type`Член шаблона класса называет тип возвращаемого значения, *вызываемого* при вызове, используя аргументы arguments.... `type`Элемент определен только в том случае, если *вызываемый* метод можно вызвать при помощи аргументов *args*... в невычисленном контексте. В противном случае шаблон класса не имеет члена `type` , что позволяет SFINAE тесты для определенного набора типов аргументов во время компиляции.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)\
[invoke](functional-functions.md#invoke)
