---
description: 'Дополнительные сведения о: Ккомклассфактори Class'
title: Класс Ккомклассфактори
ms.date: 11/04/2016
f1_keywords:
- CComClassFactory
- ATLCOM/ATL::CComClassFactory
- ATLCOM/ATL::CComClassFactory::CreateInstance
- ATLCOM/ATL::CComClassFactory::LockServer
helpviewer_keywords:
- CComClassFactory class
ms.assetid: e56dacf7-d5c4-4c42-aef4-a86d91981a1b
ms.openlocfilehash: 36233abf13c6ff6963d02bc5431286ca6c783235
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97152299"
---
# <a name="ccomclassfactory-class"></a>Класс Ккомклассфактори

Этот класс реализует интерфейс [IClassFactory](/windows/win32/api/unknwnbase/nn-unknwnbase-iclassfactory) .

## <a name="syntax"></a>Синтаксис

```
class CComClassFactory
    : public IClassFactory,
      public CComObjectRootEx<CComGlobalsThreadModel>
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккомклассфактори:: CreateInstance](#createinstance)|Создает объект указанного идентификатора CLSID.|
|[Ккомклассфактори:: Локксервер](#lockserver)|Блокирует фабрику класса в памяти.|

## <a name="remarks"></a>Комментарии

`CComClassFactory` реализует интерфейс [IClassFactory](/windows/win32/api/unknwnbase/nn-unknwnbase-iclassfactory) , который содержит методы для создания объекта определенного идентификатора CLSID, а также блокирует фабрику класса в памяти, чтобы новые объекты могли создаваться быстрее. `IClassFactory` должен быть реализован для каждого класса, регистрируемого в системном реестре и которому назначается идентификатор CLSID.

Объекты ATL обычно получают фабрику классов путем наследования от [CComCoClass](../../atl/reference/ccomcoclass-class.md). Этот класс включает макрос [DECLARE_CLASSFACTORY](aggregation-and-class-factory-macros.md#declare_classfactory), который объявляет `CComClassFactory` фабрику классов по умолчанию. Чтобы переопределить это значение по умолчанию, укажите один из `DECLARE_CLASSFACTORY` макросов *xxx* в определении класса. Например, [DECLARE_CLASSFACTORY_EX](aggregation-and-class-factory-macros.md#declare_classfactory_ex) макрос использует указанный класс для фабрики класса:

[!code-cpp[NVC_ATL_COM#8](../../atl/codesnippet/cpp/ccomclassfactory-class_1.h)]

Приведенное выше определение класса указывает, что `CMyClassFactory` будет использоваться в качестве фабрики класса по умолчанию для объекта. `CMyClassFactory` должен быть производным от `CComClassFactory` и переопределять `CreateInstance` .

ATL предоставляет три других макроса, которые объявляют фабрику класса:

- [DECLARE_CLASSFACTORY2](aggregation-and-class-factory-macros.md#declare_classfactory2) Использует [CComClassFactory2](../../atl/reference/ccomclassfactory2-class.md), который управляет созданием с помощью лицензии.

- [DECLARE_CLASSFACTORY_AUTO_THREAD](aggregation-and-class-factory-macros.md#declare_classfactory_auto_thread) Использует [ккомклассфакторяутосреад](../../atl/reference/ccomclassfactoryautothread-class.md), который создает объекты в нескольких подразделениях.

- [DECLARE_CLASSFACTORY_SINGLETON](aggregation-and-class-factory-macros.md#declare_classfactory_singleton) Использует [ккомклассфакторисинглетон](../../atl/reference/ccomclassfactorysingleton-class.md), который конструирует один объект [ккомобжектглобал](../../atl/reference/ccomobjectglobal-class.md) .

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="ccomclassfactorycreateinstance"></a><a name="createinstance"></a> Ккомклассфактори:: CreateInstance

Создает объект указанного идентификатора CLSID и получает указатель интерфейса на этот объект.

```
STDMETHOD(CreateInstance)(LPUNKNOWN pUnkOuter, REFIID riid, void** ppvObj);
```

### <a name="parameters"></a>Параметры

*пункаутер*<br/>
окне Если объект создается как часть агрегата, *пункаутер* должен быть внешним неизвестным. В противном случае *пункаутер* должен иметь значение null.

*riid*<br/>
окне IID запрашиваемого интерфейса. Если *пункаутер* не равен null, *riid* должен иметь значение `IID_IUnknown` .

*ппвобж*<br/>
заполняет Указатель на указатель интерфейса, идентифицируемый *riid*. Если объект не поддерживает этот интерфейс, *ппвобж* имеет значение null.

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

## <a name="ccomclassfactorylockserver"></a><a name="lockserver"></a> Ккомклассфактори:: Локксервер

Увеличивает и уменьшает счетчик блокировок модуля, вызывая `_Module::Lock` и `_Module::Unlock` соответственно.

```
STDMETHOD(LockServer)(BOOL fLock);
```

### <a name="parameters"></a>Параметры

*флокк*<br/>
окне Если значение равно TRUE, счетчик блокировок увеличивается; в противном случае счетчик блокировок уменьшается.

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

### <a name="remarks"></a>Комментарии

`_Module` ссылается на глобальный экземпляр [CComModule](../../atl/reference/ccommodule-class.md) или производный от него класс.

Вызов `LockServer` позволяет клиенту хранить фабрику класса, чтобы можно было быстро создавать несколько объектов.

## <a name="see-also"></a>См. также раздел

[Класс CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md)<br/>
[ккомглобалссреадмодел](atl-typedefs.md#ccomglobalsthreadmodel)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
