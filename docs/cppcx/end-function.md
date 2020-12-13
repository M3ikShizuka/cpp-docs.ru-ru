---
description: Дополнительные сведения о функции End
title: Функция end
ms.date: 01/22/2017
f1_keywords:
- collection/Windows::Foundation::Collections::end
helpviewer_keywords:
- end Function
ms.assetid: fb837bff-fc76-4bae-9096-facf0e03041c
ms.openlocfilehash: e29595e7eb403af85abdbfa18782adf1c33c308e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97341975"
---
# <a name="end-function"></a>Функция end

Возвращает итератор, указывающий на позицию после конечного элемента коллекции, для доступа к которой используется указанный параметр интерфейса.

## <a name="syntax"></a>Синтаксис

```

template <typename T>
    ::Platform::Collections::VectorIterator<T>
    end(
        IVector<T>^ v       );

template <typename T>
    ::Platform::Collections::VectorViewIterator<T>
    end(
        IVectorView<T>^ v
       );
template <typename T>
    ::Platform::Collections::InputIterator<T>
    end(
        IIterable<T>^ i
       );
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Параметр типа шаблона.

*v*<br/>
Коллекция \<T> объектов Vector или VectorView \<T> , доступ к которым осуществляется с помощью интерфейса IVector \<T> или IVectorView \<T> .

*i*<br/>
Коллекция объектов арбитрати среда выполнения Windows, доступ к которым осуществляется с помощью \<T> интерфейса иитерабле.

### <a name="return-value"></a>Возвращаемое значение

Итератор, который указывает на позицию после конечного элемента коллекции.

### <a name="remarks"></a>Комментарии

Первые две функции шаблона возвращают итераторы, а третья возвращает итератор ввода.

Объект [Platform::Collections::VectorViewIterator](../cppcx/platform-collections-vectorviewiterator-class.md) , возвращаемый `end` , является итератором прокси-сервера, хранящего элементы типа `VectorProxy<T>`. Однако объект прокси-сервера практически никогда не отображается в пользовательском коде. Дополнительные сведения см. в разделе [Collections (C++/CX)](../cppcx/collections-c-cx.md).

### <a name="requirements"></a>Требования

**Заголовок:** collection.h

**Пространство имен:** Windows::Foundation::Collections

## <a name="see-also"></a>См. также раздел

[Пространство имен Windows:: Foundation:: Collections](../cppcx/windows-foundation-collections-namespace-c-cx.md)
