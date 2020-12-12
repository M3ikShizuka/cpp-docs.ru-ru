---
description: 'Дополнительные сведения о: bad_exception классе'
title: Класс bad_exception
ms.date: 11/04/2016
f1_keywords:
- exception/std::bad_exception
helpviewer_keywords:
- bad_exception class
ms.assetid: 5ae2c4ef-c7ad-4469-8a9e-a773e86bb000
ms.openlocfilehash: 6b47facc751e1f16e033f26be284db1287e79ea8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321616"
---
# <a name="bad_exception-class"></a>Класс bad_exception

Этот класс описывает исключение, которое может быть вызвано из обработчика unexpected.

## <a name="syntax"></a>Синтаксис

```cpp
class bad_exception : public exception {};

bad_exception();
bad_exception(const bad_exception&);
bad_exception& operator=(const bad_exception&);
const char* what() const override;
```

## <a name="remarks"></a>Remarks

Обработчик [unexpected](../standard-library/exception-functions.md#unexpected) вызовет `bad_exception` вместо завершения или вместо вызова другой функции, указанной с помощью [set_unexpected](../standard-library/exception-functions.md#set_unexpected), если `bad_exception` включен в список throw функции.

Значение, возвращаемое, `what` является строкой C, определяемой реализацией. Ни одна из функций-членов не создает исключение.

Список членов, наследуемых классом `bad_exception`, см. в разделе [Класс exception](../standard-library/exception-class.md).

## <a name="example"></a>Пример

Пример использования [unexpected](../standard-library/exception-functions.md#unexpected), вызывающего `bad_exception`, см. в разделе [set_unexpected](../standard-library/exception-functions.md#set_unexpected).
