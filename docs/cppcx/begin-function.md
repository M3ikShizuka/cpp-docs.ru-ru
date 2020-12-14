---
description: Дополнительные сведения о функции begin
title: begin - функция
ms.date: 01/22/2017
f1_keywords:
- collection/Windows::Foundation::Collections::begin
helpviewer_keywords:
- begin Function
ms.assetid: 5a44fb33-e247-49fd-b7a1-4a5b42e9e1e4
ms.openlocfilehash: ae59a4b4344da520d86c216f4c9979953e16753c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97302768"
---
# <a name="begin-function"></a>begin - функция

Возвращает итератор, указывающий на начало коллекции, для доступа к которой используется указанный параметр интерфейса.

## <a name="syntax"></a>Синтаксис

```

template <typename T>
    ::Platform::Collections::VectorIterator<T>
    begin(
          IVector<T>^ v         );

template <typename T>
    ::Platform::Collections::VectorViewIterator<T>
    begin(
          IVectorView<T>^ v
         );

template <typename T>
    ::Platform::Collections::InputIterator<T>
    begin(
          IIterable<T>^ i         );
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Параметр типа шаблона.

*v*<br/>
Коллекция \<T> объектов Vector или VectorView \<T> , доступ к которым осуществляется через интерфейс IVector \<T> или IVectorView \<T> .

*i*<br/>
Коллекция произвольных среда выполнения Windows объектов, доступ к которым осуществляется через \<T> интерфейс иитерабле.

### <a name="return-value"></a>Возвращаемое значение

Итератор, который указывает на начало коллекции.

### <a name="remarks"></a>Комментарии

Первые две функции шаблона возвращают итераторы, а третья возвращает итератор ввода.

Объект VectorIterator, возвращаемый Begin, является итератором прокси-сервера, который хранит элементы типа VectorProxy \<T> . Однако объект прокси-сервера практически никогда не отображается в пользовательском коде. Дополнительные сведения см. в разделе [Collections (C++/CX)](../cppcx/collections-c-cx.md).

### <a name="requirements"></a>Требования

**Заголовок:** collection.h

**Пространство имен:** Windows::Foundation::Collections

## <a name="see-also"></a>См. также раздел

[Пространство имен Windows:: Foundation:: Collections](../cppcx/windows-foundation-collections-namespace-c-cx.md)
