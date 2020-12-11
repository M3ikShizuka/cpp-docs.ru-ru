---
description: 'Дополнительные сведения о: Ируннаблеобжектимпл Class'
title: Класс Ируннаблеобжектимпл
ms.date: 11/04/2016
f1_keywords:
- IRunnableObjectImpl
- ATLCTL/ATL::IRunnableObjectImpl
- ATLCTL/ATL::IRunnableObjectImpl::GetRunningClass
- ATLCTL/ATL::IRunnableObjectImpl::IsRunning
- ATLCTL/ATL::IRunnableObjectImpl::LockRunning
- ATLCTL/ATL::IRunnableObjectImpl::Run
- ATLCTL/ATL::IRunnableObjectImpl::SetContainedObject
helpviewer_keywords:
- containers, running controls
- IRunnableObjectImpl class
- IRunnableObject, ATL implementation
- controls [ATL], running
- controls [C++], container running in ATL
ms.assetid: 305c7c3b-889e-49dd-aca1-34379c1b9931
ms.openlocfilehash: ecae31d23eb68ce45e9b140a3e5034fb6c5400fa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97158118"
---
# <a name="irunnableobjectimpl-class"></a>Класс Ируннаблеобжектимпл

Этот класс реализует `IUnknown` интерфейс [ируннаблеобжект](/windows/win32/api/objidl/nn-objidl-irunnableobject) и предоставляет реализацию по умолчанию.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
template<class T>
class IRunnableObjectImpl
```

#### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IRunnableObjectImpl` .

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ируннаблеобжектимпл:: Жетруннингкласс](#getrunningclass)|Возвращает идентификатор CLSID выполняемого элемента управления. Реализация ATL присваивает идентификатору CLSID значение GUID_NULL и возвращает E_UNEXPECTED.|
|[Ируннаблеобжектимпл:: выполнение](#isrunning)|Определяет, работает ли элемент управления. Реализация ATL возвращает значение TRUE.|
|[Ируннаблеобжектимпл:: Локкруннинг](#lockrunning)|Блокирует элемент управления в состоянии выполнения. Реализация ATL возвращает S_OK.|
|[Ируннаблеобжектимпл:: Run](#run)|Принудительное выполнение элемента управления. Реализация ATL возвращает S_OK.|
|[Ируннаблеобжектимпл:: Сетконтаинедобжект](#setcontainedobject)|Указывает, что элемент управления внедрен. Реализация ATL возвращает S_OK.|

## <a name="remarks"></a>Комментарии

Интерфейс [ируннаблеобжект](/windows/win32/api/objidl/nn-objidl-irunnableobject) позволяет контейнеру определить, выполняется ли элемент управления, принудительно запускать его или блокировать в состояние выполнения. Класс `IRunnableObjectImpl` предоставляет реализацию этого интерфейса по умолчанию и реализует `IUnknown` , отправляя сведения в устройство дампа в отладочных сборках.

Руководство по **сопутствующим статьям** [ATL](../../atl/active-template-library-atl-tutorial.md), [Создание проекта ATL](../../atl/reference/creating-an-atl-project.md)

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IRunnableObject`

`IRunnableObjectImpl`

## <a name="requirements"></a>Требования

**Заголовок:** атлктл. h

## <a name="irunnableobjectimplgetrunningclass"></a><a name="getrunningclass"></a> Ируннаблеобжектимпл:: Жетруннингкласс

Возвращает идентификатор CLSID выполняемого элемента управления.

```
HRESULT GetRunningClass(LPCLSID lpClsid);
```

### <a name="return-value"></a>Возвращаемое значение

Реализация ATL задает для \* *лпклсид* GUID_NULL и возвращает E_UNEXPECTED.

### <a name="remarks"></a>Комментарии

См. раздел [ируннаблеобжект:: жетруннингкласс](/windows/win32/api/objidl/nf-objidl-irunnableobject-getrunningclass) в Windows SDK.

## <a name="irunnableobjectimplisrunning"></a><a name="isrunning"></a> Ируннаблеобжектимпл:: выполнение

Определяет, работает ли элемент управления.

```
virtual BOOL IsRunning();
```

### <a name="return-value"></a>Возвращаемое значение

Реализация ATL возвращает значение TRUE.

### <a name="remarks"></a>Комментарии

См. раздел [ируннаблеобжект::](/windows/win32/api/objidl/nf-objidl-irunnableobject-isrunning) Windows SDK.

## <a name="irunnableobjectimpllockrunning"></a><a name="lockrunning"></a> Ируннаблеобжектимпл:: Локкруннинг

Блокирует элемент управления в состоянии выполнения.

```
HRESULT LockRunning(BOOL fLock, BOOL fLastUnlockCloses);
```

### <a name="return-value"></a>Возвращаемое значение

Реализация ATL возвращает S_OK.

### <a name="remarks"></a>Комментарии

См. раздел [ируннаблеобжект:: локкруннинг](/windows/win32/api/objidl/nf-objidl-irunnableobject-lockrunning) в Windows SDK.

## <a name="irunnableobjectimplrun"></a><a name="run"></a> Ируннаблеобжектимпл:: Run

Принудительное выполнение элемента управления.

```
HRESULT Run(LPBINDCTX lpbc);
```

### <a name="return-value"></a>Возвращаемое значение

Реализация ATL возвращает S_OK.

### <a name="remarks"></a>Комментарии

См. раздел [ируннаблеобжект:: Run](/windows/win32/api/objidl/nf-objidl-irunnableobject-run) в Windows SDK.

## <a name="irunnableobjectimplsetcontainedobject"></a><a name="setcontainedobject"></a> Ируннаблеобжектимпл:: Сетконтаинедобжект

Указывает, что элемент управления внедрен.

```
HRESULT SetContainedObject(BOOL fContained);
```

### <a name="return-value"></a>Возвращаемое значение

Реализация ATL возвращает S_OK.

### <a name="remarks"></a>Комментарии

См. раздел [ируннаблеобжект:: сетконтаинедобжект](/windows/win32/api/objidl/nf-objidl-irunnableobject-setcontainedobject) в Windows SDK.

## <a name="see-also"></a>См. также раздел

[Класс Ккомконтрол](../../atl/reference/ccomcontrol-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
