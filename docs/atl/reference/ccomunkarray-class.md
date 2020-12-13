---
description: 'Дополнительные сведения о: Ккомункаррай Class'
title: Класс Ккомункаррай
ms.date: 11/04/2016
f1_keywords:
- CComUnkArray
- ATLCOM/ATL::CComUnkArray
- ATLCOM/ATL::CComUnkArray::CComUnkArray
- ATLCOM/ATL::CComUnkArray::Add
- ATLCOM/ATL::CComUnkArray::begin
- ATLCOM/ATL::CComUnkArray::end
- ATLCOM/ATL::CComUnkArray::GetCookie
- ATLCOM/ATL::CComUnkArray::GetUnknown
- ATLCOM/ATL::CComUnkArray::Remove
helpviewer_keywords:
- connection points [C++], managing
- CComUnkArray class
ms.assetid: 5fd4b378-a7b5-4cc1-8866-8ab72a73639e
ms.openlocfilehash: e03022fb751b487debb9f81d9e3d99ce46f1b9e7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142146"
---
# <a name="ccomunkarray-class"></a>Класс Ккомункаррай

Этот класс хранит `IUnknown` указатели и предназначен для использования в качестве параметра для класса шаблона [иконнектионпоинтимпл](../../atl/reference/iconnectionpointimpl-class.md) .

## <a name="syntax"></a>Синтаксис

```
template<unsigned int nMaxSize>
class CComUnkArray
```

#### <a name="parameters"></a>Параметры

*нмакссизе*<br/>
Максимальное число `IUnknown` указателей, которые могут храниться в статическом массиве.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккомункаррай:: Ккомункаррай](#ccomunkarray)|Конструктор.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Ккомункаррай:: Add](#add)|Вызовите этот метод, чтобы добавить `IUnknown` указатель на массив.|
|[Ккомункаррай:: Begin](#begin)|Возвращает указатель на первый `IUnknown` указатель в коллекции.|
|[Ккомункаррай:: end](#end)|Возвращает указатель на один из последних `IUnknown` указателей в коллекции.|
|[Ккомункаррай:: Кука](#getcookie)|Вызовите этот метод, чтобы получить файл cookie, связанный с заданным `IUnknown` указателем.|
|[Ккомункаррай:: неизвестный](#getunknown)|Вызовите этот метод, чтобы получить `IUnknown` указатель, связанный с заданным файлом cookie.|
|[Ккомункаррай:: Remove](#remove)|Вызовите этот метод, чтобы удалить `IUnknown` указатель из массива.|

## <a name="remarks"></a>Комментарии

`CComUnkArray` содержит фиксированное число `IUnknown` указателей, каждый из которых является интерфейсом в точке соединения. `CComUnkArray` может использоваться в качестве параметра для класса шаблона [иконнектионпоинтимпл](../../atl/reference/iconnectionpointimpl-class.md) . `CComUnkArray<1>` — это специализация шаблона `CComUnkArray` , оптимизированная для одной точки подключения.

`CComUnkArray`Методы [Begin](#begin) и [End](#end) можно использовать для выполнения цикла по всем точкам соединения (например, при срабатывании события).

Дополнительные сведения об автоматизации создания прокси-серверов точек подключения см. в разделе [Добавление точек подключения к объекту](../../atl/adding-connection-points-to-an-object.md) .

> [!NOTE]
> **Примечание** . Класс [ккомдинамикункаррай](../../atl/reference/ccomdynamicunkarray-class.md) используется мастером **добавления классов** при создании элемента управления с точками соединения. Если вы хотите вручную указать число точек соединения, измените ссылку с `CComDynamicUnkArray` на `CComUnkArray<` *n* `>` , где *n* — необходимое число точек соединения.

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="ccomunkarrayadd"></a><a name="add"></a> Ккомункаррай:: Add

Вызовите этот метод, чтобы добавить `IUnknown` указатель на массив.

```
DWORD Add(IUnknown* pUnk);
```

### <a name="parameters"></a>Параметры

*pUnk*<br/>
Вызовите этот метод, чтобы добавить `IUnknown` указатель на массив.

### <a name="return-value"></a>Возвращаемое значение

Возвращает файл cookie, связанный с вновь добавленным указателем, или значение 0, если массив недостаточно велик для размещения нового указателя.

## <a name="ccomunkarraybegin"></a><a name="begin"></a> Ккомункаррай:: Begin

Возвращает указатель на начало коллекции `IUnknown` указателей интерфейса.

```
IUnknown**
    begin();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на `IUnknown` указатель интерфейса.

### <a name="remarks"></a>Комментарии

Коллекция содержит указатели на интерфейсы, хранимые локально как `IUnknown` . Каждый интерфейс приводится `IUnknown` к реальному типу интерфейса, а затем вызывается через него. Сначала не нужно запрашивать интерфейс.

Прежде чем использовать `IUnknown` интерфейс, убедитесь, что он не РАВЕН null.

## <a name="ccomunkarrayccomunkarray"></a><a name="ccomunkarray"></a> Ккомункаррай:: Ккомункаррай

Конструктор.

```
CComUnkArray();
```

### <a name="remarks"></a>Комментарии

Задает для коллекции хранение `nMaxSize` `IUnknown` указателей и инициализирует УКАЗАТЕЛИ значением NULL.

## <a name="ccomunkarrayend"></a><a name="end"></a> Ккомункаррай:: end

Возвращает указатель на один из последних `IUnknown` указателей в коллекции.

```
IUnknown**
    end();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на `IUnknown` указатель интерфейса.

### <a name="remarks"></a>Комментарии

`CComUnkArray`Методы `begin` и `end` могут использоваться для перебора всех точек соединения, например при срабатывании события.

[!code-cpp[NVC_ATL_COM#44](../../atl/codesnippet/cpp/ccomunkarray-class_1.cpp)]

## <a name="ccomunkarraygetcookie"></a><a name="getcookie"></a> Ккомункаррай:: Кука

Вызовите этот метод, чтобы получить файл cookie, связанный с заданным `IUnknown` указателем.

```
DWORD WINAPI GetCookie(IUnknown** ppFind);
```

### <a name="parameters"></a>Параметры

*ппфинд*<br/>
`IUnknown`Указатель, для которого требуется связанный файл cookie.

### <a name="return-value"></a>Возвращаемое значение

Возвращает файл cookie, связанный с `IUnknown` указателем, или значение 0, если соответствующий `IUnknown` указатель не найден.

### <a name="remarks"></a>Комментарии

Если имеется несколько экземпляров одного и того же `IUnknown` указателя, эта функция возвращает файл cookie для первого объекта.

## <a name="ccomunkarraygetunknown"></a><a name="getunknown"></a> Ккомункаррай:: неизвестный

Вызовите этот метод, чтобы получить `IUnknown` указатель, связанный с заданным файлом cookie.

```
IUnknown* WINAPI GetUnknown(DWORD dwCookie);
```

### <a name="parameters"></a>Параметры

*двкукие*<br/>
Файл cookie, для которого `IUnknown` требуется связанный указатель.

### <a name="return-value"></a>Возвращаемое значение

Возвращает `IUnknown` указатель или значение null, если соответствующий файл cookie не найден.

## <a name="ccomunkarrayremove"></a><a name="remove"></a> Ккомункаррай:: Remove

Вызовите этот метод, чтобы удалить `IUnknown` указатель из массива.

```
BOOL Remove(DWORD dwCookie);
```

### <a name="parameters"></a>Параметры

*двкукие*<br/>
Файл cookie, ссылающийся на `IUnknown` указатель, удаляемый из массива.

### <a name="return-value"></a>Возвращаемое значение

Возвращает значение TRUE, если указатель удален, и FALSE в противном случае.

## <a name="see-also"></a>См. также раздел

[Класс Ккомдинамикункаррай](../../atl/reference/ccomdynamicunkarray-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
