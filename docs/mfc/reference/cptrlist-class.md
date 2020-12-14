---
description: 'Дополнительные сведения о: Кптрлист Class'
title: Класс Кптрлист
ms.date: 11/04/2016
f1_keywords:
- CPtrList
helpviewer_keywords:
- lists, generic
- CPtrList class [MFC]
- generic lists
ms.assetid: 4139a09c-4338-4f42-9eea-51336120b43c
ms.openlocfilehash: 27849db4687860ab68feb548de1ed8ad209b73a6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97343255"
---
# <a name="cptrlist-class"></a>Класс Кптрлист

Поддерживает списки пустых указателей.

## <a name="syntax"></a>Синтаксис

```
class CPtrList : public CObject
```

## <a name="members"></a>Члены

Функции элементов `CPtrList` похожи на функции членов класса [коблист](../../mfc/reference/coblist-class.md). Из-за этой схожести для изучения этой функции-члена можно использовать справочную документацию по классу `CObList`. Когда `CObject` указатель отображается как параметр функции или возвращаемое значение, замените указатель на **`void`** .

`CObject*& CObList::GetHead() const;`

, например, преобразуется в

`void*& CPtrList::GetHead() const;`

## <a name="remarks"></a>Комментарии

`CPtrList` включает в себя макрос IMPLEMENT_DYNAMIC для поддержки доступа к типу во время выполнения и дампа в `CDumpContext` объекте. Если требуется дамп отдельных элементов списка указателей, необходимо установить глубину контекста дампа в 1 или более.

Списки указателей не могут быть сериализованы.

При `CPtrList` удалении объекта или удалении его элементов удаляются только указатели, а не сущности, на которые они ссылаются.

Дополнительные сведения об использовании `CPtrList` см. в статье [коллекции](../../mfc/collections.md)статей.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CPtrList`

## <a name="requirements"></a>Требования

**Заголовок:** афксколл. h

## <a name="see-also"></a>См. также раздел

[CObject, класс](../../mfc/reference/cobject-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс Коблист](../../mfc/reference/coblist-class.md)
