---
description: 'Дополнительные сведения о: Ивиевобжектексимпл Class'
title: Класс Ивиевобжектексимпл
ms.date: 11/04/2016
f1_keywords:
- IViewObjectExImpl
- ATLCTL/ATL::IViewObjectExImpl
- ATLCTL/ATL::IViewObjectExImpl::Draw
- ATLCTL/ATL::IViewObjectExImpl::Freeze
- ATLCTL/ATL::IViewObjectExImpl::GetAdvise
- ATLCTL/ATL::IViewObjectExImpl::GetColorSet
- ATLCTL/ATL::IViewObjectExImpl::GetExtent
- ATLCTL/ATL::IViewObjectExImpl::GetNaturalExtent
- ATLCTL/ATL::IViewObjectExImpl::GetRect
- ATLCTL/ATL::IViewObjectExImpl::GetViewStatus
- ATLCTL/ATL::IViewObjectExImpl::QueryHitPoint
- ATLCTL/ATL::IViewObjectExImpl::QueryHitRect
- ATLCTL/ATL::IViewObjectExImpl::SetAdvise
- ATLCTL/ATL::IViewObjectExImpl::Unfreeze
helpviewer_keywords:
- ActiveX controls [C++], drawing
- IViewObjectEx ATL implementation
- advise sinks
- IViewObjectExImpl class
ms.assetid: ad6de760-1ee5-4883-b033-ae57beffc369
ms.openlocfilehash: 16b6f4a94635410f777e5c34e794ca425d38c466
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97139104"
---
# <a name="iviewobjecteximpl-class"></a>Класс Ивиевобжектексимпл

Этот класс реализует `IUnknown` и предоставляет реализации по умолчанию интерфейсов [ивиевобжект](/windows/win32/api/oleidl/nn-oleidl-iviewobject), [IViewObject2](/windows/win32/api/oleidl/nn-oleidl-iviewobject2)и [ивиевобжектекс](/windows/win32/api/ocidl/nn-ocidl-iviewobjectex) .

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<class T>
class ATL_NO_VTABLE IViewObjectExImpl
   : public IViewObjectEx
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IViewObjectExImpl` .

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ивиевобжектексимпл::D RAW](#draw)|Рисует представление элемента управления в контексте устройства.|
|[Ивиевобжектексимпл:: Freeze](#freeze)|Закрепляет отображаемое представление элемента управления, чтобы оно не изменялось до `Unfreeze` . Реализация ATL возвращает E_NOTIMPL.|
|[Ивиевобжектексимпл:: Advise](#getadvise)|Возвращает существующее соединение приемника уведомлений в элементе управления, если таковое имеется.|
|[Ивиевобжектексимпл:: Color](#getcolorset)|Возвращает логическую палитру, используемую элементом управления для рисования. Реализация ATL возвращает E_NOTIMPL.|
|[Ивиевобжектексимпл:: расширение](#getextent)|Получает отображаемый размер элемента управления в единицах HIMETRIC (0,01 миллиметра на единицу) из элемента данных класса элементов управления [ккомконтролбасе:: m_sizeExtent](../../atl/reference/ccomcontrolbase-class.md#m_sizeextent).|
|[Ивиевобжектексимпл:: Жетнатуралекстент](#getnaturalextent)|Предоставляет подсказки по размеру из контейнера для объекта, используемого при изменении его размера пользователем.|
|[Ивиевобжектексимпл:: коrect](#getrect)|Возвращает прямоугольник, описывающий запрошенный аспект рисования. Реализация ATL возвращает E_NOTIMPL.|
|[Ивиевобжектексимпл:: Жетвиевстатус](#getviewstatus)|Возвращает сведения о непрозрачности объекта и о поддерживаемых аспектах рисования.|
|[Ивиевобжектексимпл:: Куерихитпоинт](#queryhitpoint)|Проверяет, находится ли указанная точка в указанном прямоугольнике, и возвращает значение [хитресулт](/windows/win32/api/ocidl/ne-ocidl-hitresult) в `pHitResult` .|
|[Ивиевобжектексимпл:: Куерихитрект](#queryhitrect)|Проверяет, пересекается ли прямоугольник, отображаемый элементом управления, с любой точкой в указанном прямоугольнике расположения и возвращает значение ХИТРЕСУЛТ в `pHitResult` .|
|[Ивиевобжектексимпл:: Сетадвисе](#setadvise)|Устанавливает соединение между элементом управления и приемником уведомлений, чтобы приемник мог получать уведомления об изменениях в представлении элемента управления.|
|[Ивиевобжектексимпл:: unfreeze](#unfreeze)|Отменяет фиксацию отображаемого представления элемента управления. Реализация ATL возвращает E_NOTIMPL.|

## <a name="remarks"></a>Комментарии

Интерфейсы [ивиевобжект](/windows/win32/api/oleidl/nn-oleidl-iviewobject), [IViewObject2](/windows/win32/api/oleidl/nn-oleidl-iviewobject2)и [ивиевобжектекс](/windows/win32/api/ocidl/nn-ocidl-iviewobjectex) позволяют элементу управления непосредственно отображать себя, а также создавать приемник уведомлений и управлять им для уведомления контейнера об изменениях в отображении элемента управления. `IViewObjectEx`Интерфейс обеспечивает поддержку функций расширенного управления, таких как рисование без мерцания, непрямоугольные и прозрачные элементы управления, и проверка попадания (например, как близкое Нажатие мыши должно быть рассмотрено в элементе управления). Класс `IViewObjectExImpl` предоставляет реализацию этих интерфейсов по умолчанию и реализует `IUnknown` , отправляя сведения на устройство дампа в отладочных сборках.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IViewObjectEx`

`IViewObjectExImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлктл. h

## <a name="iviewobjecteximpldraw"></a><a name="draw"></a> Ивиевобжектексимпл::D RAW

Рисует представление элемента управления в контексте устройства.

```
STDMETHOD(Draw)(
    DWORD dwDrawAspect,
    LONG lindex,
    void* pvAspect,
    DVTARGETDEVICE* ptd,
    HDC hicTargetDev,
    LPCRECTL prcBounds,
    LPCRECTL prcWBounds,
    BOOL(_stdcall* /* pfnContinue*/) (DWORD_PTR dwContinue),
    DWORD_PTR /* dwContinue */);
```

### <a name="remarks"></a>Комментарии

Этот метод вызывает `CComControl::OnDrawAdvanced` , который, в свою очередь, вызывает метод класса элемента управления `OnDraw` . `OnDraw`Метод автоматически добавляется в класс элемента управления при создании элемента управления с помощью мастера элементов управления ATL. По умолчанию мастер `OnDraw` рисует прямоугольник с меткой "ATL 3,0".

См. раздел [ивиевобжект::D RAW](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw) в Windows SDK.

## <a name="iviewobjecteximplfreeze"></a><a name="freeze"></a> Ивиевобжектексимпл:: Freeze

Закрепляет отображаемое представление элемента управления, чтобы оно не изменялось до `Unfreeze` . Реализация ATL возвращает E_NOTIMPL.

```
STDMETHOD(Freeze)(
    DWORD /* dwAspect */,
    LONG /* lindex */,
    void* /* pvAspect */,
    DWORD* /* pdwFreeze */);
```

### <a name="remarks"></a>Комментарии

См. раздел [ивиевобжект:: Freeze](/windows/win32/api/oleidl/nf-oleidl-iviewobject-freeze) в Windows SDK.

## <a name="iviewobjecteximplgetadvise"></a><a name="getadvise"></a> Ивиевобжектексимпл:: Advise

Возвращает существующее соединение приемника уведомлений в элементе управления, если таковое имеется.

```
STDMETHOD(GetAdvise)(
    DWORD* /* pAspects */,
    DWORD* /* pAdvf */,
    IAdviseSink** /* ppAdvSink */);
```

### <a name="remarks"></a>Комментарии

Приемник рекомендаций хранится в элементе управления Data Control Member [ккомконтролбасе:: m_spAdviseSink](../../atl/reference/ccomcontrolbase-class.md#m_spadvisesink).

См. раздел [ивиевобжект:: unadvise](/windows/win32/api/oleidl/nf-oleidl-iviewobject-getadvise) в Windows SDK.

## <a name="iviewobjecteximplgetcolorset"></a><a name="getcolorset"></a> Ивиевобжектексимпл:: Color

Возвращает логическую палитру, используемую элементом управления для рисования. Реализация ATL возвращает E_NOTIMPL.

```
STDMETHOD(GetColorSet)(
    DWORD /* dwAspect */,
    LONG /* lindex */,
    void* /* pvAspect */,
    DVTARGETDEVICE* /* ptd */,
    HDC /* hicTargetDevice */,
    LOGPALETTE** /* ppColorSet */);
```

### <a name="remarks"></a>Комментарии

См. раздел [ивиевобжект:: Windows SDK Color](/windows/win32/api/oleidl/nf-oleidl-iviewobject-getcolorset) в.

## <a name="iviewobjecteximplgetextent"></a><a name="getextent"></a> Ивиевобжектексимпл:: расширение

Получает отображаемый размер элемента управления в единицах HIMETRIC (0,01 миллиметра на единицу) из элемента данных класса элементов управления [ккомконтролбасе:: m_sizeExtent](../../atl/reference/ccomcontrolbase-class.md#m_sizeextent).

```
STDMETHOD(GetExtent)(
    DWORD /* dwDrawAspect */,
    LONG /* lindex */,
    DVTARGETDEVICE* /* ptd */,
    LPSIZEL* lpsizel);
```

### <a name="remarks"></a>Комментарии

См. раздел [IViewObject2:: "](/windows/win32/api/oleidl/nf-oleidl-iviewobject2-getextent) в Windows SDK.

## <a name="iviewobjecteximplgetnaturalextent"></a><a name="getnaturalextent"></a> Ивиевобжектексимпл:: Жетнатуралекстент

Предоставляет подсказки по размеру из контейнера для объекта, используемого при изменении его размера пользователем.

```
STDMETHOD(GetNaturalExtent)(
    DWORD dwAspect,
    LONG /* lindex */,
    DVTARGETDEVICE* /* ptd */,
    HDC /* hicTargetDevice */,
    DVEXTENTINFO* pExtentInfo,
    LPSIZEL psizel);
```

### <a name="remarks"></a>Комментарии

Если `dwAspect` имеет значение DVASPECT_CONTENT и *пекстентинфо->двекстентмоде* является DVEXTENT_CONTENT, устанавливает * `psizel` в элемент данных класса элемента управления [ккомконтролбасе:: m_sizeNatural](../../atl/reference/ccomcontrolbase-class.md#m_sizenatural). В противном случае возвращает ошибку HRESULT.

См. раздел [ивиевобжектекс:: жетнатуралекстент](/windows/win32/api/ocidl/nf-ocidl-iviewobjectex-getnaturalextent) в Windows SDK.

## <a name="iviewobjecteximplgetrect"></a><a name="getrect"></a> Ивиевобжектексимпл:: коrect

Возвращает прямоугольник, описывающий запрошенный аспект рисования. Реализация ATL возвращает E_NOTIMPL.

```
STDMETHOD(GetRect)(DWORD /* dwAspect */, LPRECTL /* pRect */);
```

### <a name="remarks"></a>Комментарии

См. раздел [ивиевобжектекс:: коrect](/windows/win32/api/ocidl/nf-ocidl-iviewobjectex-getrect) в Windows SDK.

## <a name="iviewobjecteximplgetviewstatus"></a><a name="getviewstatus"></a> Ивиевобжектексимпл:: Жетвиевстатус

Возвращает сведения о непрозрачности объекта и о поддерживаемых аспектах рисования.

```
STDMETHOD(GetViewStatus)(DWORD* pdwStatus);
```

### <a name="remarks"></a>Комментарии

По умолчанию ATL `pdwStatus` указывает, что элемент управления поддерживает VIEWSTATUS_OPAQUE (возможные значения находятся в перечислении [виевстатус](/windows/win32/api/ocidl/ne-ocidl-viewstatus) ).

См. раздел [ивиевобжектекс:: жетвиевстатус](/windows/win32/api/ocidl/nf-ocidl-iviewobjectex-getviewstatus) в Windows SDK.

## <a name="iviewobjecteximplqueryhitpoint"></a><a name="queryhitpoint"></a> Ивиевобжектексимпл:: Куерихитпоинт

Проверяет, находится ли указанная точка в указанном прямоугольнике, и возвращает значение [хитресулт](/windows/win32/api/ocidl/ne-ocidl-hitresult) в `pHitResult` .

```
STDMETHOD(QueryHitPoint)(
    DWORD dwAspect,
    LPCRECT pRectBounds,
    POINT ptlLoc,
    LONG /* lCloseHit */,
    DWORD* /* pHitResult */);
```

### <a name="remarks"></a>Комментарии

Значение может быть либо HITRESULT_HIT, либо HITRESULT_OUTSIDE.

Если `dwAspect` значение равно [DVASPECT_CONTENT](/windows/win32/api/wtypes/ne-wtypes-dvaspect), метод возвращает S_OK. В противном случае метод возвращает E_FAIL.

См. раздел [ивиевобжектекс:: куерихитпоинт](/windows/win32/api/ocidl/nf-ocidl-iviewobjectex-queryhitpoint) в Windows SDK.

## <a name="iviewobjecteximplqueryhitrect"></a><a name="queryhitrect"></a> Ивиевобжектексимпл:: Куерихитрект

Проверяет, пересекается ли прямоугольник, отображаемый элементом управления, с любой точкой в указанном прямоугольнике расположения и возвращает значение [хитресулт](/windows/win32/api/ocidl/ne-ocidl-hitresult) в `pHitResult` .

```
STDMETHOD(QueryHitRect)(
    DWORD dwAspect,
    LPCRECT pRectBounds,
    LPRECT prcLoc,
    LONG /* lCloseHit */,
    DWORD* /* pHitResult */);
```

### <a name="remarks"></a>Комментарии

Значение может быть либо HITRESULT_HIT, либо HITRESULT_OUTSIDE.

Если `dwAspect` значение равно [DVASPECT_CONTENT](/windows/win32/api/wtypes/ne-wtypes-dvaspect), метод возвращает S_OK. В противном случае метод возвращает E_FAIL.

См. раздел [ивиевобжектекс:: куерихитрект](/windows/win32/api/ocidl/nf-ocidl-iviewobjectex-queryhitrect) в Windows SDK.

## <a name="iviewobjecteximplsetadvise"></a><a name="setadvise"></a> Ивиевобжектексимпл:: Сетадвисе

Устанавливает соединение между элементом управления и приемником уведомлений, чтобы приемник мог получать уведомления об изменениях в представлении элемента управления.

```
STDMETHOD(SetAdvise)(
    DWORD /* aspects */,
    DWORD /* advf */,
    IAdviseSink* pAdvSink);
```

### <a name="remarks"></a>Комментарии

Указатель на интерфейс [иадвисесинк](/windows/win32/api/objidl/nn-objidl-iadvisesink) в приемнике уведомлений хранится в члене данных класса элемента управления [ккомконтролбасе:: m_spAdviseSink](ccomcontrolbase-class.md#m_spadvisesink).

См. раздел [ивиевобжект:: сетадвисе](/windows/win32/api/oleidl/nf-oleidl-iviewobject-setadvise) в Windows SDK.

## <a name="iviewobjecteximplunfreeze"></a><a name="unfreeze"></a> Ивиевобжектексимпл:: unfreeze

Отменяет фиксацию отображаемого представления элемента управления. Реализация ATL возвращает E_NOTIMPL.

```
STDMETHOD(Unfreeze)(DWORD /* dwFreeze */);
```

### <a name="remarks"></a>Комментарии

См. раздел [ивиевобжект:: unfreeze](/windows/win32/api/oleidl/nf-oleidl-iviewobject-unfreeze) в Windows SDK.

## <a name="iworkerthreadclientclosehandle"></a><a name="closehandle"></a> Иворкерсреадклиент:: CloseHandle

Реализуйте этот метод, чтобы закрыть маркер, связанный с этим объектом.

```
HRESULT CloseHandle(HANDLE hHandle);
```

### <a name="parameters"></a>Параметры

*ххандле*<br/>
Закрываемый обработчик.

### <a name="return-value"></a>Возвращаемое значение

Возвращает S_OK об успешном выполнении или ошибку HRESULT при сбое.

### <a name="remarks"></a>Комментарии

Маркер, переданный этому методу, был ранее связан с этим объектом посредством вызова [кворкерсреад:: аддхандле](../../atl/reference/cworkerthread-class.md#addhandle).

### <a name="example"></a>Пример

В следующем коде показана простая реализация `IWorkerThreadClient::CloseHandle` .

[!code-cpp[NVC_ATL_Utilities#135](../../atl/codesnippet/cpp/iviewobjecteximpl-class_1.cpp)]

## <a name="iworkerthreadclientexecute"></a><a name="execute"></a> Иворкерсреадклиент:: Execute

Реализуйте этот метод для выполнения кода, когда дескриптор, связанный с этим объектом, получает сигнал.

```
HRESULT Execute(DWORD_PTR dwParam, HANDLE hObject);
```

### <a name="parameters"></a>Параметры

*двпарам*<br/>
Параметр User.

*хобжект*<br/>
Дескриптор, который стал сигнальным.

### <a name="return-value"></a>Возвращаемое значение

Возвращает S_OK об успешном выполнении или ошибку HRESULT при сбое.

### <a name="remarks"></a>Комментарии

Маркер и DWORD или указатель, переданный этому методу, ранее были связаны с этим объектом посредством вызова [кворкерсреад:: аддхандле](../../atl/reference/cworkerthread-class.md#addhandle).

### <a name="example"></a>Пример

В следующем коде показана простая реализация `IWorkerThreadClient::Execute` .

[!code-cpp[NVC_ATL_Utilities#136](../../atl/codesnippet/cpp/iviewobjecteximpl-class_2.cpp)]

## <a name="see-also"></a>См. также раздел

[Класс Ккомконтрол](../../atl/reference/ccomcontrol-class.md)<br/>
[Интерфейсы элементов управления ActiveX](/windows/win32/com/activex-controls-interfaces)<br/>
[Руководство](../../atl/active-template-library-atl-tutorial.md)<br/>
[Создание проекта ATL](../../atl/reference/creating-an-atl-project.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
