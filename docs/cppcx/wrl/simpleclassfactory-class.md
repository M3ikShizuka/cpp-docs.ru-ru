---
description: 'Дополнительные сведения о: метод simpleclassfactory Class'
title: SimpleClassFactory - класс
ms.date: 09/7/2018
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::SimpleClassFactory
- module/Microsoft::WRL::SimpleClassFactory::CreateInstance
helpviewer_keywords:
- Microsoft::WRL::SimpleClassFactory class
- Microsoft::WRL::SimpleClassFactory::CreateInstance method
ms.assetid: 6edda1b2-4e44-4e14-9364-72f519249962
ms.openlocfilehash: cd771909790f80048d8fee678b842f820e2f7be2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97135204"
---
# <a name="simpleclassfactory-class"></a>SimpleClassFactory - класс

Предоставляет основной механизм для создания базового класса.

## <a name="syntax"></a>Синтаксис

```cpp
template<typename Base>
class SimpleClassFactory : public ClassFactory<>;
```

### <a name="parameters"></a>Параметры

*Из*<br/>
Базовый класс.

## <a name="remarks"></a>Комментарии

Базовый класс должен предоставлять конструктор по умолчанию.

В следующем примере кода показано, как использовать `SimpleClassFactory` с макросом [активатаблеклассвисфакторекс](activatableclass-macros.md) .

`ActivatableClassWithFactoryEx(MyClass, SimpleClassFactory, MyServerName);`

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Метод SimpleClassFactory::CreateInstance](#createinstance)|Создает экземпляр указанного интерфейса.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`I0`

`ChainInterfaces`

`I0`

`RuntimeClassBase`

`ImplementsHelper`

`DontUseNewUseMake`

`RuntimeClassFlags`

`RuntimeClassBaseT`

`RuntimeClass`

`ClassFactory`

`SimpleClassFactory`

## <a name="requirements"></a>Требования

**Заголовок:** Module. h

**Пространство имен:** Microsoft::WRL

## <a name="simpleclassfactorycreateinstance-method"></a><a name="createinstance"></a> Метод метод simpleclassfactory:: CreateInstance

Создает экземпляр указанного интерфейса.

```cpp
STDMETHOD( CreateInstance )(
   _Inout_opt_ IUnknown* pUnkOuter,
   REFIID riid,
   _Deref_out_ void** ppvObject
);
```

#### <a name="parameters"></a>Параметры

*пункаутер*<br/>
**`nullptr`** В противном случае возвращаемое значение — CLASS_E_NOAGGREGATION.

SimpleClassFactory не поддерживает агрегирование. Если статистическая обработка поддерживалась и создаваемый объект являлся частью статистической функции, *пункаутер* бы был указателем на управляющий `IUnknown` интерфейс статистической функции.

*riid*<br/>
Идентификатор интерфейса объекта, который требуется создать.

*ппвобжект*<br/>
По завершении этой операции указатель на экземпляр объекта, указанный параметром *riid* .

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, указывающее на ошибку.

### <a name="remarks"></a>Комментарии

Если `__WRL_STRICT__` определено значение, выдается ошибка Assert, если базовый класс, указанный в параметре шаблона класса, не является производным от [RuntimeClass](runtimeclass-class.md)или не настроен с помощью значения перечисления Классикком или WinRtClassicComMix [RuntimeClassType](runtimeclasstype-enumeration.md) .
