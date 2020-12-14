---
description: 'Дополнительные сведения о: Кстринглист Class'
title: Класс Кстринглист
ms.date: 11/04/2016
f1_keywords:
- CStringList
- AFXCOLL/CStringList
- AFXCOLL/CStringList::CStringList
- AFXCOLL/CStringList::AddHead
- AFXCOLL/CStringList::AddTail
- AFXCOLL/CStringList::Find
- AFXCOLL/CStringList::FindIndex
- AFXCOLL/CStringList::GetAt
- AFXCOLL/CStringList::GetCount
- AFXCOLL/CStringList::GetHead
- AFXCOLL/CStringList::GetHeadPosition
- AFXCOLL/CStringList::GetNext
- AFXCOLL/CStringList::GetPrev
- AFXCOLL/CStringList::GetSize
- AFXCOLL/CStringList::GetTail
- AFXCOLL/CStringList::GetTailPosition
- AFXCOLL/CStringList::InsertAfter
- AFXCOLL/CStringList::InsertBefore
- AFXCOLL/CStringList::IsEmpty
- AFXCOLL/CStringList::RemoveAll
- AFXCOLL/CStringList::RemoveAt
- AFXCOLL/CStringList::RemoveHead
- AFXCOLL/CStringList::RemoveTail
- AFXCOLL/CStringList::SetAt
helpviewer_keywords:
- CStringList [MFC], CStringList
- CStringList [MFC], AddHead
- CStringList [MFC], AddTail
- CStringList [MFC], Find
- CStringList [MFC], FindIndex
- CStringList [MFC], GetAt
- CStringList [MFC], GetCount
- CStringList [MFC], GetHead
- CStringList [MFC], GetHeadPosition
- CStringList [MFC], GetNext
- CStringList [MFC], GetPrev
- CStringList [MFC], GetSize
- CStringList [MFC], GetTail
- CStringList [MFC], GetTailPosition
- CStringList [MFC], InsertAfter
- CStringList [MFC], InsertBefore
- CStringList [MFC], IsEmpty
- CStringList [MFC], RemoveAll
- CStringList [MFC], RemoveAt
- CStringList [MFC], RemoveHead
- CStringList [MFC], RemoveTail
- CStringList [MFC], SetAt
ms.assetid: 310a7edb-263c-4bd2-ac43-0bfbfddc5a33
ms.openlocfilehash: c9043ef648f50e880f3b5946c1912deca3de6714
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97345073"
---
# <a name="cstringlist-class"></a>Класс Кстринглист

Поддерживает списки объектов `CString` .

## <a name="syntax"></a>Синтаксис

```
class CStringList : public CObject
```

## <a name="members"></a>Члены

Функции элементов `CStringList` похожи на функции членов класса [коблист](../../mfc/reference/coblist-class.md). Из-за этой схожести для изучения этой функции-члена можно использовать справочную документацию по классу `CObList`. Когда `CObject` указатель отображается как возвращаемое значение, замените `CString` (не `CString` указатель). В любом месте, где вы видите `CObject` указатель в качестве параметра функции, замените `LPCTSTR` .

`CObject*& CObList::GetHead() const;`

, например, преобразуется в

`CString& CStringList::GetHead() const;`

и

`POSITION AddHead( CObject* <newElement> );`

преобразуется в

`POSITION AddHead( LPCTSTR <newElement> );`

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кстринглист:: Кстринглист](../../mfc/reference/coblist-class.md#coblist)|Конструирует пустой список.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кстринглист:: Аддхеад](../../mfc/reference/coblist-class.md#addhead)|Добавляет элемент (или все элементы из другого списка) в заголовок списка (создает новый заголовок).|
|[Кстринглист:: AddTail](../../mfc/reference/coblist-class.md#addtail)|Добавляет элемент (или все элементы из другого списка) в конец списка (создает новый хвост).|
|[Кстринглист:: Find](../../mfc/reference/coblist-class.md#find)|Возвращает расположение элемента, заданного значением указателя.|
|[Кстринглист:: FindIndex](../../mfc/reference/coblist-class.md#findindex)|Возвращает расположение элемента, указанного с помощью индекса, начинающегося с нуля.|
|[Кстринглист:: GetAt](../../mfc/reference/coblist-class.md#getat)|Возвращает элемент в заданной позиции.|
|[Кстринглист:: NOCOUNT](../../mfc/reference/coblist-class.md#getcount)|Возвращает число элементов в этом списке.|
|[Кстринглист:: onhead](../../mfc/reference/coblist-class.md#gethead)|Возвращает головной элемент списка (не может быть пустым).|
|[Кстринглист:: Жесеадпоситион](../../mfc/reference/coblist-class.md#getheadposition)|Возвращает расположение головного элемента списка.|
|[Кстринглист:: GetNext](../../mfc/reference/coblist-class.md#getnext)|Возвращает следующий элемент для итерации.|
|[Кстринглист:: prev](../../mfc/reference/coblist-class.md#getprev)|Возвращает предыдущий элемент для итерации.|
|[Кстринглист:: DataSize](../../mfc/reference/coblist-class.md#getsize)|Возвращает число элементов в этом списке.|
|[Кстринглист:: tail](../../mfc/reference/coblist-class.md#gettail)|Возвращает заключительный элемент списка (не может быть пустым).|
|[Кстринглист:: Жеттаилпоситион](../../mfc/reference/coblist-class.md#gettailposition)|Возвращает расположение элемента хвоста в списке.|
|[Кстринглист:: InsertAfter](../../mfc/reference/coblist-class.md#insertafter)|Вставляет новый элемент после заданной позицией.|
|[Кстринглист:: методов insertBefore](../../mfc/reference/coblist-class.md#insertbefore)|Вставляет новый элемент перед заданной позицией.|
|[Кстринглист:: IsEmpty](../../mfc/reference/coblist-class.md#isempty)|Проверяет условие пустого списка (нет элементов).|
|[Кстринглист:: RemoveAll](../../mfc/reference/coblist-class.md#removeall)|Удаляет все элементы из этого списка.|
|[Кстринглист:: RemoveAt](../../mfc/reference/coblist-class.md#removeat)|Удаляет элемент из этого списка, заданный по положению.|
|[Кстринглист:: Ремовехеад](../../mfc/reference/coblist-class.md#removehead)|Удаляет элемент из заголовка списка.|
|[Кстринглист:: Ремоветаил](../../mfc/reference/coblist-class.md#removetail)|Удаляет элемент из хвоста списка.|
|[Кстринглист:: SetAt](../../mfc/reference/coblist-class.md#setat)|Задает элемент в заданной позиции.|

## <a name="remarks"></a>Комментарии

Все сравнения выполняются по значению, то есть символы в строке сравниваются вместо адресов строк.

`CStringList` включает макрос IMPLEMENT_SERIAL для поддержки сериализации и дампа его элементов. Если список `CString` объектов хранится в архиве либо с перегруженным оператором вставки, либо с `Serialize` функцией-членом, каждый `CString` элемент сериализуется в свою очередь.

Если требуется дамп отдельных `CString` элементов, необходимо установить глубину контекста дампа в 1 или более.

Дополнительные сведения об использовании `CStringList` см. в статье [коллекции](../../mfc/collections.md)статей.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CStringList`

## <a name="requirements"></a>Требования

**Заголовок:** афксколл. h

## <a name="see-also"></a>См. также раздел

[Пример СОБРАНий MFC](../../overview/visual-cpp-samples.md)<br/>
[CObject, класс](../../mfc/reference/cobject-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)
