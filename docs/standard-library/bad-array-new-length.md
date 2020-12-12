---
description: 'Дополнительные сведения о: bad_array_new_length классе'
title: Класс bad_array_new_length
ms.date: 11/04/2016
f1_keywords:
- new/std::bad_array_new_length
helpviewer_keywords:
- bad_alloc class
ms.assetid: 6429a8e6-5a49-4907-8d56-f4a4ec8131d0
ms.openlocfilehash: e9de10b6fee215651ac8ff6ce2fce4af55ce6c82
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321644"
---
# <a name="bad_array_new_length-class"></a>Класс bad_array_new_length

Класс описывает исключение, которое указывает, что запрос на выделение не был успешно выполнен из-за того, что размер массива меньше нуля или больше его ограничения.

## <a name="syntax"></a>Синтаксис

```cpp
class bad_array_new_length : public bad_alloc {
    public: bad_array_new_length() noexcept;
    const char* what() const noexcept override;
};
```

## <a name="remarks"></a>Remarks

Значение, возвращаемое, `what` является строкой C, определяемой реализацией. Ни одна из функций-членов не создает исключение.

## <a name="requirements"></a>Требования

**Заголовок:**\<new>

## <a name="see-also"></a>См. также раздел

[Класс Exception](../standard-library/exception-class.md)\
[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
