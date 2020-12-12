---
description: 'Дополнительные сведения о: CD2DPathGeometry Class'
title: Класс CD2DPathGeometry
ms.date: 11/04/2016
f1_keywords:
- CD2DPathGeometry
- AFXRENDERTARGET/CD2DPathGeometry
- AFXRENDERTARGET/CD2DPathGeometry::CD2DPathGeometry
- AFXRENDERTARGET/CD2DPathGeometry::Attach
- AFXRENDERTARGET/CD2DPathGeometry::Create
- AFXRENDERTARGET/CD2DPathGeometry::Destroy
- AFXRENDERTARGET/CD2DPathGeometry::Detach
- AFXRENDERTARGET/CD2DPathGeometry::GetFigureCount
- AFXRENDERTARGET/CD2DPathGeometry::GetSegmentCount
- AFXRENDERTARGET/CD2DPathGeometry::Open
- AFXRENDERTARGET/CD2DPathGeometry::Stream
- AFXRENDERTARGET/CD2DPathGeometry::m_pPathGeometry
helpviewer_keywords:
- CD2DPathGeometry [MFC], CD2DPathGeometry
- CD2DPathGeometry [MFC], Attach
- CD2DPathGeometry [MFC], Create
- CD2DPathGeometry [MFC], Destroy
- CD2DPathGeometry [MFC], Detach
- CD2DPathGeometry [MFC], GetFigureCount
- CD2DPathGeometry [MFC], GetSegmentCount
- CD2DPathGeometry [MFC], Open
- CD2DPathGeometry [MFC], Stream
- CD2DPathGeometry [MFC], m_pPathGeometry
ms.assetid: 686216eb-5080-4242-ace5-8fa1ce96307c
ms.openlocfilehash: eb33d498436c887eb038b3312e2b98ca04d6620b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97280538"
---
# <a name="cd2dpathgeometry-class"></a>Класс CD2DPathGeometry

Оболочка для ID2D1PathGeometry.

## <a name="syntax"></a>Синтаксис

```
class CD2DPathGeometry : public CD2DGeometry;
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CD2DPathGeometry::CD2DPathGeometry](#cd2dpathgeometry)|Конструирует объект CD2DPathGeometry.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CD2DPathGeometry:: Attach](#attach)|Присоединяет существующий интерфейс ресурсов к объекту|
|[CD2DPathGeometry:: Create](#create)|Создает CD2DPathGeometry. (Переопределяет [CD2DResource:: Create](../../mfc/reference/cd2dresource-class.md#create).)|
|[CD2DPathGeometry::D естрой](#destroy)|Уничтожает объект CD2DPathGeometry. (Переопределяет [CD2DGeometry::D естрой](../../mfc/reference/cd2dgeometry-class.md#destroy).)|
|[CD2DPathGeometry::D етач](#detach)|Отсоединяет интерфейс ресурса от объекта|
|[CD2DPathGeometry:: Жетфигурекаунт](#getfigurecount)|Извлекает количество фигур в геометрии пути.|
|[CD2DPathGeometry:: Жетсегменткаунт](#getsegmentcount)|Возвращает количество сегментов в геометрии пути.|
|[CD2DPathGeometry:: Open](#open)|Извлекает геометрический приемник, используемый для заполнения геометрии контура рисунками и сегментами.|
|[CD2DPathGeometry:: Stream](#stream)|Копирует содержимое геометрии пути в указанный ID2D1GeometrySink.|

### <a name="protected-data-members"></a>Защищенные члены данных

|Имя|Описание|
|----------|-----------------|
|[CD2DPathGeometry:: m_pPathGeometry](#m_ppathgeometry)|Указатель на ID2D1PathGeometry.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CD2DResource](../../mfc/reference/cd2dresource-class.md)

[CD2DGeometry](../../mfc/reference/cd2dgeometry-class.md)

`CD2DPathGeometry`

## <a name="requirements"></a>Требования

**Заголовок:** афксрендертаржет. h

## <a name="cd2dpathgeometryattach"></a><a name="attach"></a> CD2DPathGeometry:: Attach

Присоединяет существующий интерфейс ресурсов к объекту

```cpp
void Attach(ID2D1PathGeometry* pResource);
```

### <a name="parameters"></a>Параметры

*исходный код*<br/>
Существующий интерфейс ресурсов. Не может иметь значение NULL

## <a name="cd2dpathgeometrycd2dpathgeometry"></a><a name="cd2dpathgeometry"></a> CD2DPathGeometry::CD2DPathGeometry

Конструирует объект CD2DPathGeometry.

```
CD2DPathGeometry(
    CRenderTarget* pParentTarget,
    BOOL bAutoDestroy = TRUE);
```

### <a name="parameters"></a>Параметры

*ппаренттаржет*<br/>
Указатель на целевой объект прорисовки.

*баутодестрой*<br/>
Указывает, что объект будет уничтожен владельцем (Ппаренттаржет).

## <a name="cd2dpathgeometrycreate"></a><a name="create"></a> CD2DPathGeometry:: Create

Создает CD2DPathGeometry.

```
virtual HRESULT Create(CRenderTarget* pRenderTarget);
```

### <a name="parameters"></a>Параметры

*прендертаржет*<br/>
Указатель на целевой объект прорисовки.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращает значение S_OK. В противном случае возвращается код ошибки HRESULT.

## <a name="cd2dpathgeometrydestroy"></a><a name="destroy"></a> CD2DPathGeometry::D естрой

Уничтожает объект CD2DPathGeometry.

```
virtual void Destroy();
```

## <a name="cd2dpathgeometrydetach"></a><a name="detach"></a> CD2DPathGeometry::D етач

Отсоединяет интерфейс ресурса от объекта

```
ID2D1PathGeometry* Detach();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на отсоединенный интерфейс ресурсов.

## <a name="cd2dpathgeometrygetfigurecount"></a><a name="getfigurecount"></a> CD2DPathGeometry:: Жетфигурекаунт

Извлекает количество фигур в геометрии пути.

```
int GetFigureCount() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает число цифр в геометрии пути.

## <a name="cd2dpathgeometrygetsegmentcount"></a><a name="getsegmentcount"></a> CD2DPathGeometry:: Жетсегменткаунт

Возвращает количество сегментов в геометрии пути.

```
int GetSegmentCount() const;
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает количество сегментов в геометрии пути.

## <a name="cd2dpathgeometrym_ppathgeometry"></a><a name="m_ppathgeometry"></a> CD2DPathGeometry:: m_pPathGeometry

Указатель на ID2D1PathGeometry.

```
ID2D1PathGeometry* m_pPathGeometry;
```

## <a name="cd2dpathgeometryopen"></a><a name="open"></a> CD2DPathGeometry:: Open

Извлекает геометрический приемник, используемый для заполнения геометрии контура рисунками и сегментами.

```
ID2D1GeometrySink* Open();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на ID2D1GeometrySink, используемый для заполнения геометрии контура рисунками и сегментами.

## <a name="cd2dpathgeometrystream"></a><a name="stream"></a> CD2DPathGeometry:: Stream

Копирует содержимое геометрии пути в указанный ID2D1GeometrySink.

```
BOOL Stream(ID2D1GeometrySink* geometrySink);
```

### <a name="parameters"></a>Параметры

*жеометрисинк*<br/>
Приемник, в который копируются содержимое геометрии пути. Изменение этого приемника не приводит к изменению содержимого этой геометрии пути.

### <a name="return-value"></a>Возвращаемое значение

Если метод завершается с ошибкой, возвращается значение TRUE. В противном случае возвращается значение FALSE.

## <a name="see-also"></a>См. также раздел

[Классы](../../mfc/reference/mfc-classes.md)
