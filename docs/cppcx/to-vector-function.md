---
description: Дополнительные сведения о функции to_vector
title: Функция to_vector
ms.date: 12/30/2016
f1_keywords:
- collection/Windows::Foundation::Collections::to_vector
helpviewer_keywords:
- to_vector Function
ms.assetid: 9cdd5123-7243-4def-a1d3-162e0bf6219e
ms.openlocfilehash: 77d6bee58a793946f91bc03ba4afed35aa7252cd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97307591"
---
# <a name="to_vector-function"></a>Функция to_vector

Возвращает объект `std::vector` , значение которого совпадает с коллекцией, лежащей в основе указанного параметра IVector или IVectorView.

## <a name="syntax"></a>Синтаксис

```
template <typename T>
inline ::std::vector<T> to_vector(IVector<T>^ v);

template <typename T>
inline ::std::vector<T> to_vector(IVectorView<T>^ v);
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Параметр типа шаблона.

*v*<br/>
Интерфейс IVector или IVectorView, который предоставляет доступ к базовому объекту Vector или VectorView.

### <a name="return-value"></a>Возвращаемое значение

### <a name="requirements"></a>Требования

**Заголовок:** collection.h

**Пространство имен:** Windows::Foundation::Collections

## <a name="see-also"></a>См. также раздел

[Пространство имен Windows:: Foundation:: Collections](../cppcx/windows-foundation-collections-namespace-c-cx.md)
