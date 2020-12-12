---
description: 'Подробнее о: класс CByteArray'
title: Класс CByteArray
ms.date: 11/04/2016
f1_keywords:
- CByteArray
- AFXCOLL/CByteArray
- AFXCOLL/CByteArray::CByteArray
- AFXCOLL/CByteArray::Add
- AFXCOLL/CByteArray::Append
- AFXCOLL/CByteArray::Copy
- AFXCOLL/CByteArray::ElementAt
- AFXCOLL/CByteArray::FreeExtra
- AFXCOLL/CByteArray::GetAt
- AFXCOLL/CByteArray::GetCount
- AFXCOLL/CByteArray::GetData
- AFXCOLL/CByteArray::GetSize
- AFXCOLL/CByteArray::GetUpperBound
- AFXCOLL/CByteArray::InsertAt
- AFXCOLL/CByteArray::IsEmpty
- AFXCOLL/CByteArray::RemoveAll
- AFXCOLL/CByteArray::RemoveAt
- AFXCOLL/CByteArray::SetAt
- AFXCOLL/CByteArray::SetAtGrow
- AFXCOLL/CByteArray::SetSize
helpviewer_keywords:
- CByteArray [MFC], CByteArray
- CByteArray [MFC], Add
- CByteArray [MFC], Append
- CByteArray [MFC], Copy
- CByteArray [MFC], ElementAt
- CByteArray [MFC], FreeExtra
- CByteArray [MFC], GetAt
- CByteArray [MFC], GetCount
- CByteArray [MFC], GetData
- CByteArray [MFC], GetSize
- CByteArray [MFC], GetUpperBound
- CByteArray [MFC], InsertAt
- CByteArray [MFC], IsEmpty
- CByteArray [MFC], RemoveAll
- CByteArray [MFC], RemoveAt
- CByteArray [MFC], SetAt
- CByteArray [MFC], SetAtGrow
- CByteArray [MFC], SetSize
ms.assetid: 53d4a512-657c-4187-9609-e3f5339a78e0
ms.openlocfilehash: dd1c354fa380d9eba808fb808ebfffc3b861c3bc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97122529"
---
# <a name="cbytearray-class"></a>Класс CByteArray

Поддерживает динамические массивы байтов.

## <a name="syntax"></a>Синтаксис

```
class CByteArray : public CObject
```

## <a name="members"></a>Члены

Функции элементов `CByteArray` похожи на функции членов класса [кобаррай](../../mfc/reference/cobarray-class.md). Из-за этой схожести для изучения этой функции-члена можно использовать справочную документацию по классу `CObArray`. Когда `CObject` указатель отображается как параметр функции или возвращаемое значение, подставьте байт.

`CObject* CObArray::GetAt( int <nIndex> ) const;`

, например, преобразуется в

`BYTE CByteArray::GetAt( int <nIndex> ) const;`

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CByteArray:: CByteArray](../../mfc/reference/cobarray-class.md#cobarray)|Создает пустой массив.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CByteArray:: Add](../../mfc/reference/cobarray-class.md#add)|Добавляет элемент в конец массива. При необходимости размер массива увеличивается.|
|[CByteArray:: Append](../../mfc/reference/cobarray-class.md#append)|Добавляет другой массив к массиву. При необходимости размер массива увеличивается.|
|[CByteArray:: Copy](../../mfc/reference/cobarray-class.md#copy)|Копирует другой массив в этот массив. При необходимости размер массива увеличивается.|
|[CByteArray:: ElementAt](../../mfc/reference/cobarray-class.md#elementat)|Возвращает временную ссылку на байт в массиве.|
|[CByteArray:: Фриекстра](../../mfc/reference/cobarray-class.md#freeextra)|Освобождает всю неиспользуемую память сверх текущей верхней границы.|
|[CByteArray:: GetAt](../../mfc/reference/cobarray-class.md#getat)|Возвращает значение по указанному индексу.|
|[CByteArray:: NOCOUNT](../../mfc/reference/cobarray-class.md#getcount)|Возвращает количество элементов в массиве.|
|[CByteArray:: GetData](../../mfc/reference/cobarray-class.md#getdata)|Разрешает доступ к элементам в массиве. Может иметь значение NULL.|
|[CByteArray:: DataSize](../../mfc/reference/cobarray-class.md#getsize)|Возвращает количество элементов в массиве.|
|[CByteArray:: GetUpperBound](../../mfc/reference/cobarray-class.md#getupperbound)|Возвращает самый большой допустимый индекс.|
|[CByteArray:: Инсертат](../../mfc/reference/cobarray-class.md#insertat)|Вставляет элемент (или все элементы в другом массиве) по указанному индексу.|
|[CByteArray:: IsEmpty](../../mfc/reference/cobarray-class.md#isempty)|Определяет, пуст ли массив.|
|[CByteArray:: RemoveAll](../../mfc/reference/cobarray-class.md#removeall)|Удаляет все элементы из этого массива.|
|[CByteArray:: RemoveAt](../../mfc/reference/cobarray-class.md#removeat)|Удаляет элемент по указанному индексу.|
|[CByteArray:: SetAt](../../mfc/reference/cobarray-class.md#setat)|Задает значение для указанного индекса. Размер массива не увеличивается.|
|[CByteArray:: Сетатгров](../../mfc/reference/cobarray-class.md#setatgrow)|Задает значение для указанного индекса. При необходимости размер массива увеличивается.|
|[CByteArray:: SetSize](../../mfc/reference/cobarray-class.md#setsize)|Задает число элементов, которые будут храниться в этом массиве.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Оператор CByteArray:: operator \[\]](../../mfc/reference/cobarray-class.md#operator_at)|Получает или задает элемент с указанным индексом.|

## <a name="remarks"></a>Комментарии

`CByteArray` включает макрос IMPLEMENT_SERIAL для поддержки сериализации и дампа его элементов. Если массив байтов хранится в архиве с перегруженным **<<** оператором вставки () или с `Serialize` функцией-членом, каждый элемент в свою очередь сериализуется.

> [!NOTE]
> Перед работой с массивом используйте функцию `SetSize`, чтобы определить его размер и выделить под него память. Если не использовать функцию `SetSize`, при добавлении элементов в массив он будет часто копироваться и для него снова и снова будет повторно выделяться память. Это может привести к ухудшению производительности и фрагментации памяти.

Если требуется вывод отладки из отдельных элементов в массиве, необходимо задать `CDumpContext` для глубины объекта значение 1 или больше.

Дополнительные сведения об использовании `CByteArray` см. в статье [коллекции](../../mfc/collections.md)статей.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CByteArray`

## <a name="requirements"></a>Требования

**Заголовок:** афксколл. h

## <a name="see-also"></a>См. также раздел

[CObject, класс](../../mfc/reference/cobject-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Кобаррай](../../mfc/reference/cobarray-class.md)
