---
description: 'Дополнительные сведения о: RuntimeClass Class'
title: Класс RuntimeClass
ms.date: 09/11/2018
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::RuntimeClass
- implements/Microsoft::WRL::RuntimeClass::AddRef
- implements/Microsoft::WRL::RuntimeClass::DecrementReference
- implements/Microsoft::WRL::RuntimeClass::GetIids
- implements/Microsoft::WRL::RuntimeClass::GetRuntimeClassName
- implements/Microsoft::WRL::RuntimeClass::GetTrustLevel
- implements/Microsoft::WRL::RuntimeClass::GetWeakReference
- implements/Microsoft::WRL::RuntimeClass::InternalAddRef
- implements/Microsoft::WRL::RuntimeClass::QueryInterface
- implements/Microsoft::WRL::RuntimeClass::Release
- implements/Microsoft::WRL::RuntimeClass::RuntimeClass
- implements/Microsoft::WRL::RuntimeClass::~RuntimeClass
helpviewer_keywords:
- Microsoft::WRL::RuntimeClass class
- Microsoft::WRL::RuntimeClass::AddRef method
- Microsoft::WRL::RuntimeClass::DecrementReference method
- Microsoft::WRL::RuntimeClass::GetIids method
- Microsoft::WRL::RuntimeClass::GetRuntimeClassName method
- Microsoft::WRL::RuntimeClass::GetTrustLevel method
- Microsoft::WRL::RuntimeClass::GetWeakReference method
- Microsoft::WRL::RuntimeClass::InternalAddRef method
- Microsoft::WRL::RuntimeClass::QueryInterface method
- Microsoft::WRL::RuntimeClass::Release method
- Microsoft::WRL::RuntimeClass::RuntimeClass, constructor
- Microsoft::WRL::RuntimeClass::~RuntimeClass, destructor
ms.assetid: d52f9d1a-98e5-41f2-a143-8fb629dd0727
ms.openlocfilehash: f62eec0b5ac9b8fc8ecac390ea07077743fdcb51
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330760"
---
# <a name="runtimeclass-class"></a>Класс RuntimeClass

Представляет класс WinRT или COM, который наследует указанные интерфейсы и предоставляет указанную среда выполнения Windows, классическую модель COM и поддержку слабых ссылок.

Этот класс предоставляет стандартную реализацию классов WinRT и com, предоставляя реализацию, и `QueryInterface` `AddRef` `Release` т. д., управляет счетчиком ссылок модуля и поддерживает предоставление фабрики класса для объектов активируемого.

## <a name="syntax"></a>Синтаксис

```cpp
template <typename ...TInterfaces> class RuntimeClass
template <unsigned int classFlags, typename ...TInterfaces> class RuntimeClass;
```

### <a name="parameters"></a>Параметры

*классфлагс*<br/>
Необязательный параметр. Сочетание одного или нескольких значений перечисления [RuntimeClassType](runtimeclasstype-enumeration.md) . `__WRL_CONFIGURATION_LEGACY__`Макрос можно определить, чтобы изменить значение по умолчанию классфлагс для всех классов среды выполнения в проекте. Если этот параметр определен, экземпляры RuntimeClass по умолчанию не являются гибкими. Если не определено, экземпляры RuntimeClass по умолчанию являются гибкими. Во избежание неоднозначности всегда указывайте `Microsoft::WRL::FtmBase` в `TInterfaces` или `RuntimeClassType::InhibitFtmBase` . Обратите внимание, что если используются и Инхибитфтмбасе, и метод FtmBase, объект будет гибким.

*тинтерфацес*<br/>
Список интерфейсов, которые объект реализует за пределами `IUnknown` , `IInspectable` или другие интерфейсы, управляемые [RuntimeClassType](runtimeclasstype-enumeration.md). В нем также могут содержаться другие классы, от которых следует сделать, особенно `Microsoft::WRL::FtmBase` Сделайте объект гибким и привлечет его реализацию `IMarshal` .

## <a name="members"></a>Элементы

`RuntimeClassInitialize`<br/>
Функция, которая инициализирует объект, если `MakeAndInitialize` для создания объекта используется функция шаблона. Он возвращает S_OK, если объект был успешно инициализирован, или код ошибки COM, если инициализация завершилась неудачно. Код ошибки COM распространяется как возвращаемое значение `MakeAndInitialize` . Обратите внимание, что `RuntimeClassInitialize` метод не вызывается, если `Make` для создания объекта используется функция шаблона.

### <a name="public-constructors"></a>Открытые конструкторы

| name                                               | Описание                                                     |
| -------------------------------------------------- | --------------------------------------------------------------- |
| [RuntimeClass:: RuntimeClass](#runtimeclass)        | Инициализирует текущий экземпляр `RuntimeClass` класса.   |
| [RuntimeClass:: ~ RuntimeClass](#tilde-runtimeclass) | Выполняет деинициализацию текущего экземпляра `RuntimeClass` класса. |

### <a name="public-methods"></a>Открытые методы

| name                                                      | Описание                                                                                        |
| --------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| [RuntimeClass:: AddRef](#addref)                           | Увеличивает значение счетчика ссылок для текущего `RuntimeClass` объекта.                              |
| [RuntimeClass::D Екрементреференце](#decrementreference)   | Уменьшает значение счетчика ссылок для текущего `RuntimeClass` объекта.                              |
| [RuntimeClass:: GetIids](#getiids)                         | Возвращает массив, который может содержать идентификаторы интерфейса, реализованные текущим `RuntimeClass` объектом. |
| [RuntimeClass:: GetRuntimeClassName](#getruntimeclassname) | Возвращает имя класса среды выполнения для текущего `RuntimeClass` объекта.                                  |
| [RuntimeClass:: GetTrustLevel](#gettrustlevel)             | Возвращает уровень доверия текущего `RuntimeClass` объекта.                                         |
| [RuntimeClass:: GetWeakReference](#getweakreference)       | Возвращает указатель на объект слабой ссылки для текущего `RuntimeClass` объекта.                 |
| [RuntimeClass:: InternalAddRef](#internaladdref)           | Увеличивает значение счетчика ссылок до текущего `RuntimeClass` объекта.                               |
| [RuntimeClass:: QueryInterface](#queryinterface)           | Извлекает указатель на указанный идентификатор интерфейса.                                                 |
| [RuntimeClass:: Release](#release)                         | Выполняет операцию освобождения COM для текущего `RuntimeClass` объекта.                             |

## <a name="inheritance-hierarchy"></a>Иерархия наследования

Это сведения о реализации примера.

## <a name="requirements"></a>Требования

**Заголовок:** Implements. h

**Пространство имен:** Microsoft::WRL

## <a name="runtimeclassruntimeclass"></a><a name="tilde-runtimeclass"></a> RuntimeClass:: ~ RuntimeClass

Выполняет деинициализацию текущего экземпляра `RuntimeClass` класса.

```cpp
virtual ~RuntimeClass();
```

## <a name="runtimeclassaddref"></a><a name="addref"></a> RuntimeClass:: AddRef

Увеличивает значение счетчика ссылок для текущего `RuntimeClass` объекта.

```cpp
STDMETHOD_(
   ULONG,
   AddRef
)();
```

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, указывающее на ошибку.

## <a name="runtimeclassdecrementreference"></a><a name="decrementreference"></a> RuntimeClass::D Екрементреференце

Уменьшает значение счетчика ссылок для текущего `RuntimeClass` объекта.

```cpp
ULONG DecrementReference();
```

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, указывающее на ошибку.

## <a name="runtimeclassgetiids"></a><a name="getiids"></a> RuntimeClass:: GetIids

Возвращает массив, который может содержать идентификаторы интерфейса, реализованные текущим `RuntimeClass` объектом.

```cpp
STDMETHOD(
   GetIids
)
   (_Out_ ULONG *iidCount,
   _Deref_out_ _Deref_post_cap_(*iidCount) IID **iids);
```

### <a name="parameters"></a>Параметры

*iidCount*<br/>
По завершении этой операции общее число элементов в массиве *идентификаторов IID*.

*идентификаторов IID*<br/>
После завершения операции представляет указатель на массив идентификаторов интерфейса.

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение E_OUTOFMEMORY.

## <a name="runtimeclassgetruntimeclassname"></a><a name="getruntimeclassname"></a> RuntimeClass:: GetRuntimeClassName

Возвращает имя класса среды выполнения для текущего `RuntimeClass` объекта.

```cpp
STDMETHOD( GetRuntimeClassName )(
    _Out_ HSTRING* runtimeName
);
```

### <a name="parameters"></a>Параметры

*рунтименаме*<br/>
После завершения операции представляет имя класса среды выполнения.

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, указывающее на ошибку.

### <a name="remarks"></a>Комментарии

Если `__WRL_STRICT__` не определено или, возникает ошибка Assert `__WRL_FORCE_INSPECTABLE_CLASS_MACRO__` .

## <a name="runtimeclassgettrustlevel"></a><a name="gettrustlevel"></a> RuntimeClass:: GetTrustLevel

Возвращает уровень доверия текущего `RuntimeClass` объекта.

```cpp
STDMETHOD(GetTrustLevel)(
    _Out_ TrustLevel* trustLvl
);
```

### <a name="parameters"></a>Параметры

*трустлвл*<br/>
По завершении этой операции уровень доверия текущего `RuntimeClass` объекта.

### <a name="return-value"></a>Возвращаемое значение

Всегда S_OK.

### <a name="remarks"></a>Комментарии

Если `__WRL_STRICT__` не определено или, возникает ошибка Assert `__WRL_FORCE_INSPECTABLE_CLASS_MACRO__` .

## <a name="runtimeclassgetweakreference"></a><a name="getweakreference"></a> RuntimeClass:: GetWeakReference

Возвращает указатель на объект слабой ссылки для текущего `RuntimeClass` объекта.

```cpp
STDMETHOD(
   GetWeakReference
)(_Deref_out_ IWeakReference **weakReference);
```

### <a name="parameters"></a>Параметры

*weakReference*<br/>
После завершения операции представляет указатель на объект слабой ссылки.

### <a name="return-value"></a>Возвращаемое значение

Всегда S_OK.

## <a name="runtimeclassinternaladdref"></a><a name="internaladdref"></a> RuntimeClass:: InternalAddRef

Увеличивает значение счетчика ссылок до текущего `RuntimeClass` объекта.

```cpp
ULONG InternalAddRef();
```

### <a name="return-value"></a>Возвращаемое значение

Результирующий счетчик ссылок.

## <a name="runtimeclassqueryinterface"></a><a name="queryinterface"></a> RuntimeClass:: QueryInterface

Извлекает указатель на указанный идентификатор интерфейса.

```cpp
STDMETHOD(
   QueryInterface
)
   (REFIID riid,
   _Deref_out_ void **ppvObject);
```

### <a name="parameters"></a>Параметры

*riid*<br/>
Идентификатор интерфейса.

*ппвобжект*<br/>
После завершения этого опереатион указатель на интерфейс, указанный параметром *riid* .

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, указывающее на ошибку.

## <a name="runtimeclassrelease"></a><a name="release"></a> RuntimeClass:: Release

Выполняет операцию освобождения COM для текущего `RuntimeClass` объекта.

```cpp
STDMETHOD_(
   ULONG,
   Release
)();
```

### <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, указывающее на ошибку.

### <a name="remarks"></a>Комментарии

Если значение счетчика ссылок становится равным нулю, `RuntimeClass` объект удаляется.

## <a name="runtimeclassruntimeclass"></a><a name="runtimeclass"></a> RuntimeClass:: RuntimeClass

Инициализирует текущий экземпляр `RuntimeClass` класса.

```cpp
RuntimeClass();
```
