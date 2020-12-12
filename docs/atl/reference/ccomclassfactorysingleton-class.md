---
description: 'Дополнительные сведения о: Ккомклассфакторисинглетон Class'
title: Класс Ккомклассфакторисинглетон
ms.date: 11/04/2016
f1_keywords:
- CComClassFactorySingleton
- ATLCOM/ATL::CComClassFactorySingleton
- ATLCOM/ATL::CComClassFactorySingleton::CreateInstance
- ATLCOM/ATL::CComClassFactorySingleton::m_spObj
helpviewer_keywords:
- CComClassFactorySingleton class
ms.assetid: debb983c-382b-487b-8d42-7ea26dc158b8
ms.openlocfilehash: eaf09f823a6d8d62f102e6e36116b56270248f9e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97146865"
---
# <a name="ccomclassfactorysingleton-class"></a>Класс Ккомклассфакторисинглетон

Этот класс является производным от [ккомклассфактори](../../atl/reference/ccomclassfactory-class.md) и использует [ккомобжектглобал](../../atl/reference/ccomobjectglobal-class.md) для создания одного объекта.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<class T>
class CComClassFactorySingleton : public CComClassFactory
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Ваш класс.

`CComClassFactorySingleton` является производным от [ккомклассфактори](../../atl/reference/ccomclassfactory-class.md) и использует [ккомобжектглобал](../../atl/reference/ccomobjectglobal-class.md) для создания одного объекта. Каждый вызов `CreateInstance` метода просто запрашивает этот объект для указателя интерфейса.

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккомклассфакторисинглетон:: CreateInstance](#createinstance)|Запросы `m_spObj` для указателя интерфейса.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Ккомклассфакторисинглетон:: m_spObj](#m_spobj)|Объект [ккомобжектглобал](../../atl/reference/ccomobjectglobal-class.md) , созданный `CComClassFactorySingleton` .|

## <a name="remarks"></a>Комментарии

Объекты ATL обычно получают фабрику классов путем наследования от [CComCoClass](../../atl/reference/ccomcoclass-class.md). Этот класс включает макрос [DECLARE_CLASSFACTORY](aggregation-and-class-factory-macros.md#declare_classfactory), который объявляет `CComClassFactory` фабрику классов по умолчанию. Чтобы использовать `CComClassFactorySingleton` , укажите [DECLARE_CLASSFACTORY_SINGLETON](aggregation-and-class-factory-macros.md#declare_classfactory_singleton) макрос в определении класса объекта. Пример:

[!code-cpp[NVC_ATL_COM#10](../../atl/codesnippet/cpp/ccomclassfactorysingleton-class_1.h)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`CComObjectRootBase`

[CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md)

`IClassFactory`

[ккомклассфактори](../../atl/reference/ccomclassfactory-class.md)

`CComClassFactorySingleton`

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="ccomclassfactorysingletoncreateinstance"></a><a name="createinstance"></a> Ккомклассфакторисинглетон:: CreateInstance

Вызывает метод `QueryInterface` с помощью [m_spObj](#m_spobj) для получения указателя интерфейса.

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

## <a name="ccomclassfactorysingletonm_spobj"></a><a name="m_spobj"></a> Ккомклассфакторисинглетон:: m_spObj

Объект [ккомобжектглобал](../../atl/reference/ccomobjectglobal-class.md) , созданный `CComClassFactorySingleton` .

```
CComPtr<IUnknown> m_spObj;
```

### <a name="remarks"></a>Комментарии

Каждый вызов метода [CreateInstance](#createinstance) просто запрашивает этот объект для указателя интерфейса.

Обратите внимание, что в текущей форме `m_spObj` представлены критические изменения, выполняемые `CComClassFactorySingleton` в предыдущих версиях ATL. В предыдущих версиях `CComClassFactorySingleton` объект был создан в то же время, что и фабрика класса, во время инициализации сервера. В Visual C++ .NET 2003 и более поздних версиях объект создается отложенно при первом запросе. Это изменение может привести к ошибкам в программах, которые используют раннюю инициализацию.

## <a name="see-also"></a>См. также раздел

[IClassFactory](/windows/win32/api/unknwnbase/nn-unknwnbase-iclassfactory)<br/>
[Класс CComClassFactory2](../../atl/reference/ccomclassfactory2-class.md)<br/>
[Класс Ккомклассфакторяутосреад](../../atl/reference/ccomclassfactoryautothread-class.md)<br/>
[Класс CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md)<br/>
[ккомглобалссреадмодел](atl-typedefs.md#ccomglobalsthreadmodel)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
