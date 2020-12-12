---
description: 'Дополнительные сведения: слабые ссылки и циклы прерывания (C++/CX)'
title: Слабые ссылки и устранение циклов (C++/CX)
ms.date: 01/22/2017
ms.assetid: 1acb6402-05f0-4951-af94-0e9dab41c53e
ms.openlocfilehash: 0c42081b0030ee697eab63fa519e2f6cbe4fe090
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97288026"
---
# <a name="weak-references-and-breaking-cycles-ccx"></a>Слабые ссылки и устранение циклов (C++/CX)

В любой системе типов, которая основана на подсчете ссылок, ссылки на типы могут сформировать *циклы*, т. е. может возникнуть ситуация, когда один объект ссылается на второй объект, второй объект ссылается на третий объект, и так далее до тех пор, пока некоторый последний объект не будет ссылаться на первый объект. В цикле объекты невозможно правильно удалить, если количество ссылок одного из объектов становится равным нулю. Чтобы помочь вам решить эту проблему, C++/CX предоставляет класс [класса Platform:: WeakReference](../cppcx/platform-weakreference-class.md) . Объект `WeakReference` поддерживает метод [Resolve](../cppcx/platform-weakreference-class.md#resolve) , который возвращает значение NULL, если объект больше не существует, или исключение [Platform::InvalidCastException](../cppcx/platform-invalidcastexception-class.md) , если объект существует, но его тип отличается от `T`.

Один из сценариев, в котором `WeakReference` следует использовать, — это когда **`this`** указатель захватывается в лямбда-выражении, которое используется для определения обработчика событий. Рекомендуется использовать при определении обработчиков событий именованные методы, но если необходимо использовать для обработчика событий лямбда-выражения или если необходимо нарушить цикл подсчета ссылок, используйте класс `WeakReference`. Ниже приведен пример:

```

using namespace Platform::Details;
using namespace Windows::UI::Xaml;
using namespace Windows::UI::Xaml::Input;
using namespace Windows::UI::Xaml::Controls;

Class1::Class1()
{
    // Class1 has a reference to m_Page
    m_Page = ref new Page();

    // m_Page will have a reference to this Class1
    // so create a weak reference to this
    WeakReference wr(this);
    m_Page->DoubleTapped += ref new DoubleTappedEventHandler(
        [wr](Object^ sender, DoubleTappedRoutedEventArgs^ args)
    {
       // Use the weak reference to get the object
       Class1^ c = wr.Resolve<Class1>();
       if (c != nullptr)
       {
           c->m_eventFired = true;
       }
       else
       {
           // Inform the event that this handler should be removed
           // from the subscriber list
           throw ref new DisconnectedException();
       }
    });
}

}
```

Когда обработчик событий создает исключение `DisconnectedException`, событие удаляет обработчик из списка подписчиков.
