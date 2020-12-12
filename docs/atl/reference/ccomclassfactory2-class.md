---
description: 'Дополнительные сведения о: CComClassFactory2 Class'
title: Класс CComClassFactory2
ms.date: 11/04/2016
f1_keywords:
- CComClassFactory2
- ATLCOM/ATL::CComClassFactory2
- ATLCOM/ATL::CComClassFactory2::CreateInstance
- ATLCOM/ATL::CComClassFactory2::CreateInstanceLic
- ATLCOM/ATL::CComClassFactory2::GetLicInfo
- ATLCOM/ATL::CComClassFactory2::LockServer
- ATLCOM/ATL::CComClassFactory2::RequestLicKey
helpviewer_keywords:
- CComClassFactory2 class
ms.assetid: 19b66fd6-b9ed-47a0-822c-8132184f5a3e
ms.openlocfilehash: 7aebf09616c7fc4e85f6c44aee4db84886033f8b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97146891"
---
# <a name="ccomclassfactory2-class"></a>Класс CComClassFactory2

Этот класс реализует интерфейс [IClassFactory2](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) .

## <a name="syntax"></a>Синтаксис

```
template <class license>
class CComClassFactory2 : public IClassFactory2,
    public CComObjectRootEx<CComGlobalsThreadModel>,
    public license
```

#### <a name="parameters"></a>Параметры

*лицензии*<br/>
Класс, реализующий следующие статические функции:

- `static BOOL VerifyLicenseKey( BSTR bstr );`

- `static BOOL GetLicenseKey( DWORD dwReserved, BSTR * pBstr );`

- `static BOOL IsLicenseValid( );`

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CComClassFactory2:: CreateInstance](#createinstance)|Создает объект указанного идентификатора CLSID.|
|[CComClassFactory2:: Креатеинстанцелик](#createinstancelic)|При наличии лицензионного ключа создает объект указанного идентификатора CLSID.|
|[CComClassFactory2:: ЖетлиЦинфо](#getlicinfo)|Получает сведения, описывающие возможности лицензирования фабрики классов.|
|[CComClassFactory2:: Локксервер](#lockserver)|Блокирует фабрику класса в памяти.|
|[CComClassFactory2:: Рекуестликкэй](#requestlickey)|Создает и возвращает лицензионный ключ.|

## <a name="remarks"></a>Комментарии

`CComClassFactory2` реализует интерфейс [IClassFactory2](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) , который является расширением [IClassFactory](/windows/win32/api/unknwnbase/nn-unknwnbase-iclassfactory). `IClassFactory2` управляет созданием объектов с помощью лицензии. Фабрика класса, выполняемая на Лицензированном компьютере, может предоставить лицензионный ключ. Этот лицензионный ключ позволяет приложению создавать экземпляры объектов, если лицензия на компьютер не существует.

Объекты ATL обычно получают фабрику классов путем наследования от [CComCoClass](../../atl/reference/ccomcoclass-class.md). Этот класс включает макрос [DECLARE_CLASSFACTORY](aggregation-and-class-factory-macros.md#declare_classfactory), объявляющий [ккомклассфактори](../../atl/reference/ccomclassfactory-class.md) в качестве фабрики классов по умолчанию. Чтобы использовать `CComClassFactory2` , укажите [DECLARE_CLASSFACTORY2](aggregation-and-class-factory-macros.md#declare_classfactory2) макрос в определении класса объекта. Пример:

[!code-cpp[NVC_ATL_COM#2](../../atl/codesnippet/cpp/ccomclassfactory2-class_1.h)]

`CMyLicense`, параметр шаблона для `CComClassFactory2` должен реализовывать статические функции `VerifyLicenseKey` , `GetLicenseKey` и `IsLicenseValid` . Ниже приведен пример простого класса License:

[!code-cpp[NVC_ATL_COM#3](../../atl/codesnippet/cpp/ccomclassfactory2-class_2.h)]

`CComClassFactory2` является производным от `CComClassFactory2Base` *лицензии* и. `CComClassFactory2Base`, в свою очередь, является производным от `IClassFactory2` и `CComObjectRootEx< CComGlobalsThreadModel >` .

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CComObjectRootBase`

`license`

[CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md)

`IClassFactory2`

`CComClassFactory2`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="ccomclassfactory2createinstance"></a><a name="createinstance"></a> CComClassFactory2:: CreateInstance

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

### <a name="remarks"></a>Комментарии

Требует полной лицензии на компьютер. Если полная лицензия компьютера не существует, вызовите [креатеинстанцелик](#createinstancelic).

## <a name="ccomclassfactory2createinstancelic"></a><a name="createinstancelic"></a> CComClassFactory2:: Креатеинстанцелик

Аналогично [CreateInstance](#createinstance), за исключением того, что `CreateInstanceLic` требует лицензионный ключ.

```
STDMETHOD(CreateInstanceLic)(
    IUnknown* pUnkOuter,
    IUnknown* /* pUnkReserved
*/,
    REFIID riid,
    BSTR bstrKey,
    void** ppvObject);
```

### <a name="parameters"></a>Параметры

*пункаутер*<br/>
окне Если объект создается как часть агрегата, *пункаутер* должен быть внешним неизвестным. В противном случае *пункаутер* должен иметь значение null.

*пункресервед*<br/>
[in] Не используется. Должен иметь значение NULL.

*riid*<br/>
окне IID запрашиваемого интерфейса. Если *пункаутер* не равен null, *riid* должен иметь значение `IID_IUnknown` .

*бстркэй*<br/>
окне Лицензионный ключ, полученный ранее при вызове `RequestLicKey` . Этот ключ необходим для создания объекта.

*ппвобжект*<br/>
заполняет Указатель на указатель интерфейса, заданный параметром *riid*. Если объект не поддерживает этот интерфейс, *ппвобжект* имеет значение null.

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

### <a name="remarks"></a>Комментарии

Получить лицензионный ключ можно с помощью [рекуестликкэй](#requestlickey). Чтобы создать объект на компьютере, не имеющем лицензии, необходимо вызвать `CreateInstanceLic` .

## <a name="ccomclassfactory2getlicinfo"></a><a name="getlicinfo"></a> CComClassFactory2:: ЖетлиЦинфо

Заполняет структуру [лиЦинфо](/windows/win32/api/ocidl/ns-ocidl-licinfo) информацией, описывающей возможности лицензирования фабрики класса.

```
STDMETHOD(GetLicInfo)(LICINFO* pLicInfo);
```

### <a name="parameters"></a>Параметры

*плиЦинфо*<br/>
заполняет Указатель на `LICINFO` структуру.

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

### <a name="remarks"></a>Комментарии

`fRuntimeKeyAvail`Член этой структуры указывает, позволяет ли фабрика классов создавать объекты на нелицензированном компьютере с учетом лицензионного ключа. Член *фликверифиед* указывает, существует ли полная лицензия на компьютер.

## <a name="ccomclassfactory2lockserver"></a><a name="lockserver"></a> CComClassFactory2:: Локксервер

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

## <a name="ccomclassfactory2requestlickey"></a><a name="requestlickey"></a> CComClassFactory2:: Рекуестликкэй

Создает и возвращает лицензионный ключ при условии, что `fRuntimeKeyAvail` член структуры [лиЦинфо](/windows/win32/api/ocidl/ns-ocidl-licinfo) имеет значение true.

```
STDMETHOD(RequestLicKey)(DWORD dwReserved, BSTR* pbstrKey);
```

### <a name="parameters"></a>Параметры

*двресервед*<br/>
[in] Не используется. Должен равняться нулю.

*пбстркэй*<br/>
заполняет Указатель на лицензионный ключ.

### <a name="return-value"></a>Возвращаемое значение

Стандартное значение HRESULT.

### <a name="remarks"></a>Комментарии

Для вызова [креатеинстанцелик](#createinstancelic) требуется лицензионный ключ для создания объекта на нелицензированном компьютере. Если `fRuntimeKeyAvail` имеет значение false, то объекты можно создавать только на полностью лицензированном компьютере.

Вызовите [жетлиЦинфо](#getlicinfo) , чтобы получить значение `fRuntimeKeyAvail` .

## <a name="see-also"></a>См. также раздел

[Класс Ккомклассфакторяутосреад](../../atl/reference/ccomclassfactoryautothread-class.md)<br/>
[Класс Ккомклассфакторисинглетон](../../atl/reference/ccomclassfactorysingleton-class.md)<br/>
[Класс CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md)<br/>
[ккомглобалссреадмодел](atl-typedefs.md#ccomglobalsthreadmodel)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
