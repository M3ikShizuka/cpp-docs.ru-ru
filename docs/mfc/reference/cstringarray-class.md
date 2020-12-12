---
description: 'Дополнительные сведения о: Кстрингаррай Class'
title: Класс Кстрингаррай
ms.date: 11/04/2016
f1_keywords:
- CStringArray
- AFXCOLL/CStringArray
- AFXCOLL/CStringArray::CStringArray
- AFXCOLL/CStringArray::Add
- AFXCOLL/CStringArray::Append
- AFXCOLL/CStringArray::Copy
- AFXCOLL/CStringArray::ElementAt
- AFXCOLL/CStringArray::FreeExtra
- AFXCOLL/CStringArray::GetAt
- AFXCOLL/CStringArray::GetCount
- AFXCOLL/CStringArray::GetData
- AFXCOLL/CStringArray::GetSize
- AFXCOLL/CStringArray::GetUpperBound
- AFXCOLL/CStringArray::InsertAt
- AFXCOLL/CStringArray::IsEmpty
- AFXCOLL/CStringArray::RemoveAll
- AFXCOLL/CStringArray::RemoveAt
- AFXCOLL/CStringArray::SetAt
- AFXCOLL/CStringArray::SetAtGrow
- AFXCOLL/CStringArray::SetSize
helpviewer_keywords:
- CStringArray [MFC], CStringArray
- CStringArray [MFC], Add
- CStringArray [MFC], Append
- CStringArray [MFC], Copy
- CStringArray [MFC], ElementAt
- CStringArray [MFC], FreeExtra
- CStringArray [MFC], GetAt
- CStringArray [MFC], GetCount
- CStringArray [MFC], GetData
- CStringArray [MFC], GetSize
- CStringArray [MFC], GetUpperBound
- CStringArray [MFC], InsertAt
- CStringArray [MFC], IsEmpty
- CStringArray [MFC], RemoveAll
- CStringArray [MFC], RemoveAt
- CStringArray [MFC], SetAt
- CStringArray [MFC], SetAtGrow
- CStringArray [MFC], SetSize
ms.assetid: 6c637e06-bba8-4c08-b0fc-cf8cb067ce34
ms.openlocfilehash: 7f9f8579545d79eaeaf2db9616a34040b4d8e038
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97318615"
---
# <a name="cstringarray-class"></a>Класс Кстрингаррай

Поддерживает массивы объектов [CString](../../atl-mfc-shared/using-cstring.md) .

## <a name="syntax"></a>Синтаксис

```
class CStringArray : public CObject
```

## <a name="members"></a>Члены

Функции элементов `CStringArray` похожи на функции членов класса [кобаррай](../../mfc/reference/cobarray-class.md). Из-за этой схожести для изучения этой функции-члена можно использовать справочную документацию по классу `CObArray`. Когда `CObject` указатель отображается как возвращаемое значение, замените объект [CString](../../atl-mfc-shared/using-cstring.md) (а не указатель [CString](../../atl-mfc-shared/using-cstring.md) ). Если вы видите указатель `CObject` как параметр функции, замените `LPCTSTR`.

`CObject* CObArray::GetAt( int <nIndex> ) const;`

, например, преобразуется в

`CString CStringArray::GetAt( int <nIndex> ) const;`

и

`void SetAt( int <nIndex>, CObject* <newElement> )`

преобразуется в

`void SetAt( int <nIndex>, LPCTSTR <newElement> )`

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кстрингаррай:: Кстрингаррай](../../mfc/reference/cobarray-class.md#cobarray)|Создает пустой массив.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кстрингаррай:: Add](../../mfc/reference/cobarray-class.md#add)|Добавляет элемент в конец массива. При необходимости размер массива увеличивается.|
|[Кстрингаррай:: Append](../../mfc/reference/cobarray-class.md#append)|Добавляет другой массив к массиву. При необходимости размер массива увеличивается.|
|[Кстрингаррай:: Copy](../../mfc/reference/cobarray-class.md#copy)|Копирует другой массив в этот массив. При необходимости размер массива увеличивается.|
|[Кстрингаррай:: ElementAt](../../mfc/reference/cobarray-class.md#elementat)|Возвращает временную ссылку на указатель элемента в массиве.|
|[Кстрингаррай:: Фриекстра](../../mfc/reference/cobarray-class.md#freeextra)|Освобождает всю неиспользуемую память сверх текущей верхней границы.|
|[Кстрингаррай:: GetAt](../../mfc/reference/cobarray-class.md#getat)|Возвращает значение по указанному индексу.|
|[Кстрингаррай:: NOCOUNT](../../mfc/reference/cobarray-class.md#getcount)|Возвращает количество элементов в массиве.|
|[Кстрингаррай:: GetData](../../mfc/reference/cobarray-class.md#getdata)|Разрешает доступ к элементам в массиве. Может иметь **значение NULL**.|
|[Кстрингаррай:: DataSize](../../mfc/reference/cobarray-class.md#getsize)|Возвращает количество элементов в массиве.|
|[Кстрингаррай:: GetUpperBound](../../mfc/reference/cobarray-class.md#getupperbound)|Возвращает самый большой допустимый индекс.|
|[Кстрингаррай:: Инсертат](../../mfc/reference/cobarray-class.md#insertat)|Вставляет элемент (или все элементы в другом массиве) по указанному индексу.|
|[Кстрингаррай:: IsEmpty](../../mfc/reference/cobarray-class.md#isempty)|Определяет, пуст ли массив.|
|[Кстрингаррай:: RemoveAll](../../mfc/reference/cobarray-class.md#removeall)|Удаляет все элементы из этого массива.|
|[Кстрингаррай:: RemoveAt](../../mfc/reference/cobarray-class.md#removeat)|Удаляет элемент по указанному индексу.|
|[Кстрингаррай:: SetAt](../../mfc/reference/cobarray-class.md#setat)|Задает значение для указанного индекса. Размер массива не увеличивается.|
|[Кстрингаррай:: Сетатгров](../../mfc/reference/cobarray-class.md#setatgrow)|Задает значение для указанного индекса. При необходимости размер массива увеличивается.|
|[Кстрингаррай:: SetSize](../../mfc/reference/cobarray-class.md#setsize)|Задает число элементов, которые будут храниться в этом массиве.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Кстрингаррай:: operator \[\]](../../mfc/reference/cobarray-class.md#operator_at)|Получает или задает элемент с указанным индексом.|

## <a name="remarks"></a>Комментарии

`CStringArray` включает макрос IMPLEMENT_SERIAL для поддержки сериализации и дампа его элементов. Если массив объект `CString` сохраняется в архив с помощью перегруженного оператора вставки или функции-члена `Serialize`, каждый элемент сериализуется.

> [!NOTE]
> Перед работой с массивом используйте функцию `SetSize`, чтобы определить его размер и выделить под него память. Если не использовать функцию `SetSize`, при добавлении элементов в массив он будет часто копироваться и для него снова и снова будет повторно выделяться память. Это может привести к ухудшению производительности и фрагментации памяти.

Если вам требуется дамп отдельных строковых элементов в массиве, задайте для глубины контекста дампа 1 или большее значение.

При удалении массива `CString` или его элементов, строковая память освобождается соответствующим образом.

Дополнительные сведения об использовании `CStringArray` см. в статье [коллекции](../../mfc/collections.md)статей.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CStringArray`

## <a name="requirements"></a>Требования

**Заголовок:** афксколл. h

## <a name="see-also"></a>См. также раздел

[CObject, класс](../../mfc/reference/cobject-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)
