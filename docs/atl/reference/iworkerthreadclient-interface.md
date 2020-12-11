---
description: 'Дополнительные сведения о: интерфейс Иворкерсреадклиент'
title: Интерфейс Иворкерсреадклиент
ms.date: 11/04/2016
f1_keywords:
- IWorkerThreadClient
- ATLUTIL/ATL::IWorkerThreadClient
- ATLUTIL/ATL::CloseHandle
- ATLUTIL/ATL::Execute
helpviewer_keywords:
- IWorkerThreadClient interface
ms.assetid: 56f4a2f5-007e-4a33-9e20-05187629f715
ms.openlocfilehash: fb9113c9380453dad9f647fa2f5a2095ff12cea7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97157988"
---
# <a name="iworkerthreadclient-interface"></a>Интерфейс Иворкерсреадклиент

`IWorkerThreadClient` — Это интерфейс, реализуемый клиентами класса [кворкерсреад](../../atl/reference/cworkerthread-class.md) .

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
__interface IWorkerThreadClient
```

## <a name="members"></a>Члены

### <a name="methods"></a>Методы

|Имя|Описание|
|-|-|
|[CloseHandle](#closehandle)|Реализуйте этот метод, чтобы закрыть маркер, связанный с этим объектом.|
|[Execute](#execute)|Реализуйте этот метод для выполнения кода, когда дескриптор, связанный с этим объектом, получает сигнал.|

## <a name="remarks"></a>Комментарии

Реализуйте этот интерфейс, если у вас есть код, который должен выполняться в рабочем потоке в ответ на то, что дескриптор становится сигнальным.

## <a name="requirements"></a>Требования

**Заголовок:** файлов atlutil. h

## <a name="iworkerthreadclientclosehandle"></a><a name="closehandle"></a> Иворкерсреадклиент:: CloseHandle

Реализуйте этот метод, чтобы закрыть маркер, связанный с этим объектом.

```
HRESULT CloseHandle(HANDLE  hHandle);
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

[!code-cpp[NVC_ATL_Utilities#135](../../atl/codesnippet/cpp/iworkerthreadclient-interface_1.cpp)]

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

[!code-cpp[NVC_ATL_Utilities#136](../../atl/codesnippet/cpp/iworkerthreadclient-interface_2.cpp)]

## <a name="see-also"></a>См. также раздел

[Классы](../../atl/reference/atl-classes.md)<br/>
[Класс Кворкерсреад](../../atl/reference/cworkerthread-class.md)
