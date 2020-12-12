---
description: 'Дополнительные сведения о: Ккомклассфакторяутосреад Class'
title: Класс Ккомклассфакторяутосреад
ms.date: 11/04/2016
f1_keywords:
- CComClassFactoryAutoThread
- ATLCOM/ATL::CComClassFactoryAutoThread
- ATLCOM/ATL::CComClassFactoryAutoThread::CreateInstance
- ATLCOM/ATL::CComClassFactoryAutoThread::LockServer
helpviewer_keywords:
- CComClassFactoryAutoThread class
ms.assetid: 22008042-533f-4dd9-bf7e-191ee571f9a1
ms.openlocfilehash: 9d25303d4d40f695c68fdf09aae7d56e6f1e5fb1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97152286"
---
# <a name="ccomclassfactoryautothread-class"></a>Класс Ккомклассфакторяутосреад

Этот класс реализует интерфейс [IClassFactory](/windows/win32/api/unknwnbase/nn-unknwnbase-iclassfactory) и позволяет создавать объекты в нескольких подразделениях.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
class CComClassFactoryAutoThread
    : public IClassFactory,
      public CComObjectRootEx<CComGlobalsThreadModel>
```

## <a name="members"></a>Члены

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккомклассфакторяутосреад:: CreateInstance](#createinstance)|Создает объект указанного идентификатора CLSID.|
|[Ккомклассфакторяутосреад:: Локксервер](#lockserver)|Блокирует фабрику класса в памяти.|

## <a name="remarks"></a>Комментарии

`CComClassFactoryAutoThread` аналогичен [ккомклассфактори](../../atl/reference/ccomclassfactory-class.md), но позволяет создавать объекты в нескольких апартаментах. Чтобы воспользоваться этой поддержкой, создайте свой модуль EXE из [ккомаутосреадмодуле](../../atl/reference/ccomautothreadmodule-class.md).

Объекты ATL обычно получают фабрику классов путем наследования от [CComCoClass](../../atl/reference/ccomcoclass-class.md). Этот класс включает макрос [DECLARE_CLASSFACTORY](aggregation-and-class-factory-macros.md#declare_classfactory), объявляющий [ккомклассфактори](../../atl/reference/ccomclassfactory-class.md) в качестве фабрики классов по умолчанию. Чтобы использовать `CComClassFactoryAutoThread` , укажите [DECLARE_CLASSFACTORY_AUTO_THREAD](aggregation-and-class-factory-macros.md#declare_classfactory_auto_thread) макрос в определении класса объекта. Пример:

[!code-cpp[NVC_ATL_COM#9](../../atl/codesnippet/cpp/ccomclassfactoryautothread-class_1.h)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CComObjectRootBase`

[CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md)

`IClassFactory`

`CComClassFactoryAutoThread`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="ccomclassfactoryautothreadcreateinstance"></a><a name="createinstance"></a> Ккомклассфакторяутосреад:: CreateInstance

Создает объект указанного идентификатора CLSID и получает указатель интерфейса на этот объект.

```
STDMETHODIMP CreateInstance(
    LPUNKNOWN pUnkOuter,
    REFIID riid,
    void** ppvObj);
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

### <a name="remarks"></a>Комментарии

Если модуль является производным от [ккомаутосреадмодуле](../../atl/reference/ccomautothreadmodule-class.md), `CreateInstance` сначала выбирает поток для создания объекта в связанном апартаменте.

## <a name="ccomclassfactoryautothreadlockserver"></a><a name="lockserver"></a> Ккомклассфакторяутосреад:: Локксервер

Увеличивает и уменьшает счетчик блокировок модуля, вызывая `_Module::Lock` и `_Module::Unlock` соответственно.

```
STDMETHODIMP LockServer(BOOL fLock);
```

### <a name="parameters"></a>Параметры

*флокк*<br/>
окне Если значение равно TRUE, счетчик блокировок увеличивается; в противном случае счетчик блокировок уменьшается.

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

### <a name="remarks"></a>Комментарии

При использовании `CComClassFactoryAutoThread` `_Module` обычно относится к глобальному экземпляру [ккомаутосреадмодуле](../../atl/reference/ccomautothreadmodule-class.md).

Вызов `LockServer` позволяет клиенту хранить фабрику класса, чтобы можно было быстро создавать несколько объектов.

## <a name="see-also"></a>См. также раздел

[IClassFactory](/windows/win32/api/unknwnbase/nn-unknwnbase-iclassfactory)<br/>
[Класс CComClassFactory2](../../atl/reference/ccomclassfactory2-class.md)<br/>
[Класс Ккомклассфакторисинглетон](../../atl/reference/ccomclassfactorysingleton-class.md)<br/>
[Класс CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md)<br/>
[ккомглобалссреадмодел](atl-typedefs.md#ccomglobalsthreadmodel)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
