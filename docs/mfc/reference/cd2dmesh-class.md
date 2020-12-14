---
description: 'Дополнительные сведения о: CD2DMesh Class'
title: Класс CD2DMesh
ms.date: 11/04/2016
f1_keywords:
- CD2DMesh
- AFXRENDERTARGET/CD2DMesh
- AFXRENDERTARGET/CD2DMesh::CD2DMesh
- AFXRENDERTARGET/CD2DMesh::Attach
- AFXRENDERTARGET/CD2DMesh::Create
- AFXRENDERTARGET/CD2DMesh::Destroy
- AFXRENDERTARGET/CD2DMesh::Detach
- AFXRENDERTARGET/CD2DMesh::Get
- AFXRENDERTARGET/CD2DMesh::IsValid
- AFXRENDERTARGET/CD2DMesh::Open
- AFXRENDERTARGET/CD2DMesh::m_pMesh
helpviewer_keywords:
- CD2DMesh [MFC], CD2DMesh
- CD2DMesh [MFC], Attach
- CD2DMesh [MFC], Create
- CD2DMesh [MFC], Destroy
- CD2DMesh [MFC], Detach
- CD2DMesh [MFC], Get
- CD2DMesh [MFC], IsValid
- CD2DMesh [MFC], Open
- CD2DMesh [MFC], m_pMesh
ms.assetid: 11a2c78a-1367-40e8-a34f-44aa0509a4c9
ms.openlocfilehash: fbdb941d04b87df5c136f1925445564caab63443
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97193374"
---
# <a name="cd2dmesh-class"></a>Класс CD2DMesh

Оболочка для ID2D1Mesh.

## <a name="syntax"></a>Синтаксис

```
class CD2DMesh : public CD2DResource;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DMesh::CD2DMesh](#cd2dmesh)|Конструирует объект CD2DMesh.|
|[CD2DMesh:: ~ CD2DMesh](#_dtorcd2dmesh)|Деструктор Вызывается при уничтожении объекта сетки D2D.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CD2DMesh:: Attach](#attach)|Присоединяет существующий интерфейс ресурсов к объекту|
|[CD2DMesh:: Create](#create)|Создает CD2DMesh. (Переопределяет [CD2DResource:: Create](../../mfc/reference/cd2dresource-class.md#create).)|
|[CD2DMesh::D естрой](#destroy)|Уничтожает объект CD2DMesh. (Переопределяет [CD2DResource::D естрой](../../mfc/reference/cd2dresource-class.md#destroy).)|
|[CD2DMesh::D етач](#detach)|Отсоединяет интерфейс ресурса от объекта|
|[CD2DMesh:: Get](#get)|Возвращает интерфейс ID2D1Mesh|
|[CD2DMesh:: IsValid](#isvalid)|Проверяет допустимость ресурса (переопределяет [CD2DResource:: IsValid](../../mfc/reference/cd2dresource-class.md#isvalid).)|
|[CD2DMesh:: Open](#open)|Открывает сетку для заполнения.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CD2DMesh:: operator ID2D1Mesh *](#operator_id2d1mesh_star)|Возвращает интерфейс ID2D1Mesh|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CD2DMesh:: m_pMesh](#m_pmesh)|Указатель на ID2D1Mesh.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CD2DResource](../../mfc/reference/cd2dresource-class.md)

`CD2DMesh`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dmeshcd2dmesh"></a><a name="_dtorcd2dmesh"></a> CD2DMesh:: ~ CD2DMesh

Деструктор Вызывается при уничтожении объекта сетки D2D.

```
virtual ~CD2DMesh();
```

## <a name="cd2dmeshattach"></a><a name="attach"></a> CD2DMesh:: Attach

Присоединяет существующий интерфейс ресурсов к объекту

```cpp
void Attach(ID2D1Mesh* pResource);
```

### <a name="parameters"></a>Параметры

*исходный код*<br/>
Существующий интерфейс ресурсов. Не может иметь значение NULL

## <a name="cd2dmeshcd2dmesh"></a><a name="cd2dmesh"></a> CD2DMesh::CD2DMesh

Конструирует объект CD2DMesh.

```
CD2DMesh(
    CRenderTarget* pParentTarget,
    BOOL bAutoDestroy = TRUE);
```

### <a name="parameters"></a>Параметры

*ппаренттаржет*<br/>
Указатель на целевой объект прорисовки.

*баутодестрой*<br/>
Указывает, что объект будет уничтожен владельцем (Ппаренттаржет).

## <a name="cd2dmeshcreate"></a><a name="create"></a> CD2DMesh:: Create

Создает CD2DMesh.

```
virtual HRESULT Create(CRenderTarget* pRenderTarget);
```

### <a name="parameters"></a>Параметры

*прендертаржет*<br/>
Указатель на целевой объект прорисовки.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="cd2dmeshdestroy"></a><a name="destroy"></a> CD2DMesh::D естрой

Уничтожает объект CD2DMesh.

```
virtual void Destroy();
```

## <a name="cd2dmeshdetach"></a><a name="detach"></a> CD2DMesh::D етач

Отсоединяет интерфейс ресурса от объекта

```
ID2D1Mesh* Detach();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на отсоединенный интерфейс ресурсов.

## <a name="cd2dmeshget"></a><a name="get"></a> CD2DMesh:: Get

Возвращает интерфейс ID2D1Mesh

```
ID2D1Mesh* Get();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1Mesh или значение NULL, если объект еще не инициализирован.

## <a name="cd2dmeshisvalid"></a><a name="isvalid"></a> CD2DMesh:: IsValid

Проверка действительности ресурсов

```
virtual BOOL IsValid() const;
```

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если ресурс является допустимым; в противном случае — FALSE.

## <a name="cd2dmeshm_pmesh"></a><a name="m_pmesh"></a> CD2DMesh:: m_pMesh

Указатель на ID2D1Mesh.

```
ID2D1Mesh* m_pMesh;
```

## <a name="cd2dmeshopen"></a><a name="open"></a> CD2DMesh:: Open

Открывает сетку для заполнения.

```
ID2D1TessellationSink* Open();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на объект ID2D1TessellationSink, который используется для заполнения сетки.

## <a name="cd2dmeshoperator-id2d1mesh"></a><a name="operator_id2d1mesh_star"></a> CD2DMesh:: operator ID2D1Mesh *

Возвращает интерфейс ID2D1Mesh

```
operator ID2D1Mesh*();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на интерфейс ID2D1Mesh или значение NULL, если объект еще не инициализирован.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
