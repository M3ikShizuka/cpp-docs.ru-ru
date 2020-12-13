---
description: 'Дополнительные сведения о: метод simpleactivationfactory Class'
title: SimpleActivationFactory - класс
ms.date: 09/07/2018
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::SimpleActivationFactory
- module/Microsoft::WRL::SimpleActivationFactory::ActivateInstance
- module/Microsoft::WRL::SimpleActivationFactory::GetRuntimeClassName
- module/Microsoft::WRL::SimpleActivationFactory::GetTrustLevel
helpviewer_keywords:
- Microsoft::WRL::SimpleActivationFactory class
- Microsoft::WRL::SimpleActivationFactory::ActivateInstance method
- Microsoft::WRL::SimpleActivationFactory::GetRuntimeClassName method
- Microsoft::WRL::SimpleActivationFactory::GetTrustLevel method
ms.assetid: aff768e0-0038-4fd7-95d2-ad7d308da41c
ms.openlocfilehash: 83643c69977b887e58e430bbd500fcf7c2e81ca6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97135217"
---
# <a name="simpleactivationfactory-class"></a>SimpleActivationFactory - класс

Предоставляет основной механизм для создания базового класса среды выполнения Windows или классической модели COM.

## <a name="syntax"></a>Синтаксис

```cpp
template<typename Base>
class SimpleActivationFactory : public ActivationFactory<>;
```

### <a name="parameters"></a>Параметры

*Из*<br/>
Базовый класс.

## <a name="remarks"></a>Комментарии

Базовый класс должен предоставлять конструктор по умолчанию.

В следующем примере кода показано, как использовать метод simpleactivationfactory с макросом [активатаблеклассвисфакторекс](activatableclass-macros.md) .

`ActivatableClassWithFactoryEx(MyClass, SimpleActivationFactory, MyServerName);`

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Метод SimpleActivationFactory::ActivateInstance](#activateinstance)|Создает экземпляр указанного интерфейса.|
|[Метод SimpleActivationFactory::GetRuntimeClassName](#getruntimeclassname)|Возвращает имя класса среды выполнения для экземпляра класса, заданного параметром шаблона *базового* класса.|
|[Метод SimpleActivationFactory::GetTrustLevel](#gettrustlevel)|Возвращает уровень доверия экземпляра класса, заданного параметром шаблона *базового* класса.|

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

`ActivationFactory`

`SimpleActivationFactory`

## <a name="requirements"></a>Требования

**Заголовок:** Module. h

**Пространство имен:** Microsoft::WRL

## <a name="simpleactivationfactoryactivateinstance-method"></a><a name="activateinstance"></a> Метод метод simpleactivationfactory:: ActivateInstance

Создает экземпляр указанного интерфейса.

```cpp
STDMETHOD( ActivateInstance )(
    _Deref_out_ IInspectable **ppvObject
);
```

#### <a name="parameters"></a>Параметры

*ппвобжект*<br/>
По завершении этой операции указатель на экземпляр объекта, указанный `Base` параметром шаблона класса.

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, указывающее на ошибку.

### <a name="remarks"></a>Комментарии

Если `__WRL_STRICT__` определено значение, выдается ошибка Assert, если базовый класс, указанный в параметре шаблона класса, не является производным от [RuntimeClass](runtimeclass-class.md)или не настроен с помощью значения перечисления WinRt или WinRtClassicComMix [RuntimeClassType](runtimeclasstype-enumeration.md) .

## <a name="simpleactivationfactorygetruntimeclassname-method"></a><a name="getruntimeclassname"></a> Метод метод simpleactivationfactory:: GetRuntimeClassName

Получает имя класса среды выполнения экземпляра класса, указанного в параметре шаблона класса `Base`.

```cpp
STDMETHOD( GetRuntimeClassName )(
    _Out_ HSTRING* runtimeName
);
```

#### <a name="parameters"></a>Параметры

*рунтименаме*<br/>
После завершения операции представляет имя класса среды выполнения.

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, указывающее на ошибку.

### <a name="remarks"></a>Комментарии

Если `__WRL_STRICT__` определено значение, выдается ошибка Assert, если класс, указанный `Base` параметром шаблона класса, не является производным от [RuntimeClass](runtimeclass-class.md)или не настроен с помощью значения перечисления WinRt или WinRtClassicComMix [RuntimeClassType](runtimeclasstype-enumeration.md) .

## <a name="simpleactivationfactorygettrustlevel-method"></a><a name="gettrustlevel"></a> Метод метод simpleactivationfactory:: GetTrustLevel

Возвращает уровень доверия экземпляра класса, заданного `Base` параметром шаблона класса.

```cpp
STDMETHOD(
   GetTrustLevel
)(_Out_ TrustLevel* trustLvl);
```

#### <a name="parameters"></a>Параметры

*трустлвл*<br/>
По завершении этой операции уровень доверия текущего объекта класса.

### <a name="return-value"></a>Возвращаемое значение

Всегда S_OK.
