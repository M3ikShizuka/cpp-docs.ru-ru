---
description: 'Дополнительные сведения о платформе:: Metadata:: Рунтимекласснаме'
title: Platform::Metadata::RuntimeClassName
ms.date: 12/30/2016
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::Metadata::RuntimeClassName
helpviewer_keywords:
- RuntimeClassName
- Platform::Metadata::RuntimeClassName
ms.assetid: fdef8f85-ab94-4edd-ba50-ee0da9358ff6
ms.openlocfilehash: 25d6f3ae6b7509029b08f809fa20d5bd0ca5e735
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97308384"
---
# <a name="platformmetadataruntimeclassname"></a>Platform::Metadata::RuntimeClassName

При применении к определению класса, проверяет, возвращает ли функция GetRuntimeClassName допустимое имя в закрытый класс.

## <a name="syntax"></a>Синтаксис

```cpp
[Platform::Metadata::RuntimeClassName] name
```

#### <a name="parameters"></a>Параметры

*name*<br/>
Имя существующего открытого типа, который виден в среде выполнения Windows.

### <a name="remarks"></a>Комментарии

Этот атрибут используется в закрытых классах ссылок для указания имени пользовательского типа среды выполнения. Задает в качестве имени открытый интерфейс, реализуемый классом.

### <a name="example"></a>Пример

В следующем примере показано использование атрибута. В этом примере имя типа среды выполнения HellowWorldImpl является интерфейсом Test::Native::MyComponent::IHelloWorld.

```cpp
namespace Test
{
    namespace Native
    {
        namespace MyComponent
        {
            public interface class IHelloWorld
            {
                Platform::String^ SayHello();
            };

            private ref class HelloWorldImpl sealed :[Platform::Metadata::RuntimeClassName] IHelloWorld
            {
            public:
                HelloWorldImpl();
                virtual Platform::String^ SayHello();
            };

            Platform::String^ HelloWorldImpl::SayHello()
            {
                return L"Hello World!";
            }
        }
    }
}
```

## <a name="see-also"></a>См. также раздел

[Пространство имен Platform:: Metadata](../cppcx/platform-metadata-namespace.md)
