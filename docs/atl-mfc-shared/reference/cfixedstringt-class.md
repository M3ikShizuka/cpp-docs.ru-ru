---
description: 'Дополнительные сведения о: CFixedStringT Class'
title: Класс CFixedStringT
ms.date: 03/27/2019
f1_keywords:
- CFixedStringT
- CSTRINGT/ATL::CFixedStringT
- CSTRINGT/ATL::CFixedStringT::CFixedStringT
helpviewer_keywords:
- CFixedStringT class
- shared classes, CFixedStringT
ms.assetid: 6d4171ba-3104-493a-a6cc-d515f4ba9a4b
ms.openlocfilehash: a613716364318ced140709d2b33e9d9c4299af0b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97166840"
---
# <a name="cfixedstringt-class"></a>Класс CFixedStringT

Этот класс представляет строковый объект с фиксированным буфером символов.

## <a name="syntax"></a>Синтаксис

```
template<class StringType, int t_nChars>
class CFixedStringT : private CFixedStringMgr, public StringType
```

#### <a name="parameters"></a>Параметры

*StringType*<br/>
Используется в качестве базового класса для фиксированного строкового объекта и может быть любым `CStringT` типом на основе. Некоторые примеры включают `CString` , `CStringA` и `CStringW` .

*t_nChars*<br/>
Число символов, хранящихся в буфере.

## <a name="members"></a>Элементы

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[CFixedStringT:: CFixedStringT](#cfixedstringt)|Конструктор для объекта строки.|

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[CFixedStringT:: operator =](#operator_eq)|Присваивает новое значение `CFixedStringT` объекту.|

## <a name="remarks"></a>Комментарии

Этот класс является примером пользовательского класса строк на основе `CStringT` . Хотя и аналогично, эти два класса различаются в реализации. Основные различия между `CFixedStringT` и `CStringT` :

- Начальный буфер символов выделяется как часть объекта и имеет размер *t_nChars*. Это позволяет `CFixedString` объекту занимать непрерывный фрагмент памяти в целях повышения производительности. Однако если содержимое `CFixedStringT` объекта выходит за пределы *t_nChars*, буфер выделяется динамически.

- Символьный буфер для `CFixedStringT` объекта всегда имеет одинаковую длину ( *t_nChars*). Ограничения на размер буфера для `CStringT` объектов отсутствуют.

- Диспетчер памяти для `CFixedStringT` настроен таким, что совместное использование объекта [кстрингдата](../../atl-mfc-shared/reference/cstringdata-class.md) между двумя или более `CFixedStringT` объектами не допускается. `CStringT` объекты не имеют этого ограничения.

Дополнительные сведения о настройке `CFixedStringT` и управлении памятью для строковых объектов в целом см. в разделе [Управление памятью и CStringT](../../atl-mfc-shared/memory-management-with-cstringt.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`IAtlStringMgr`

`StringType`

`CFixedStringMgr`

`CFixedStringT`

## <a name="requirements"></a>Требования

**Заголовок:** CStringT. h

## <a name="cfixedstringtcfixedstringt"></a><a name="cfixedstringt"></a> CFixedStringT:: CFixedStringT

Формирует объект `CFixedStringT`.

```
CFixedStringT() throw();
explicit CFixedStringT(IAtlStringMgr* pStringMgr) throw();
CFixedStringT(const CFixedStringT<StringType, t_nChars>& strSrc);
CFixedStringT(const StringType& strSrc);
CFixedStringT(const StringType::XCHAR* pszSrc);
explicit CFixedStringT(const StringType::YCHAR* pszSrc);
explicit CFixedStringT(const unsigned char* pszSrc);
```

### <a name="parameters"></a>Параметры

*псзсрк*<br/>
Строка, завершающаяся нулем, для копирования в этот `CFixedStringT` объект.

*стрсрк*<br/>
Существующий `CFixedStringT` объект, который будет скопирован в этот `CFixedStringT` объект.

*пстрингмгр*<br/>
Указатель на диспетчер памяти `CFixedStringT` объекта. Дополнительные сведения о `IAtlStringMgr` и управлении памятью для `CFixedStringT` см. в разделе [Управление памятью и CStringT](../../atl-mfc-shared/memory-management-with-cstringt.md).

### <a name="remarks"></a>Комментарии

Поскольку конструкторы копируют входные данные в новое выделенное хранилище, следует помнить, что могут возникнуть исключения памяти. Некоторые из этих конструкторов действуют как функции преобразования.

## <a name="cfixedstringtoperator-"></a><a name="operator_eq"></a> CFixedStringT:: operator =

Повторно инициализирует существующий `CFixedStringT` объект новыми данными.

```
CFixedStringT<StringType, t_nChars>& operator=(
    const CFixedStringT<StringType, t_nChars>& strSrc);
CFixedStringT<StringType, t_nChars>& operator=(const char* pszSrc);
CFixedStringT<StringType, t_nChars>& operator=(const wchar_t* pszSrc);
CFixedStringT<StringType, t_nChars>& operator=(const unsigned char* pszSrc);
CFixedStringT<StringType, t_nChars>& operator=(const StringType& strSrc);
```

### <a name="parameters"></a>Параметры

*псзсрк*<br/>
Строка, завершающаяся нулем, для копирования в этот `CFixedStringT` объект.

*стрсрк*<br/>
Объект, существующий `CFixedStringT` для копирования в этот `CFixedStringT` объект.

### <a name="remarks"></a>Комментарии

Следует иметь в виду, что исключения памяти могут возникать при использовании оператора присваивания, поскольку для хранения результирующего объекта часто выделяется новое хранилище `CFixedStringT` .

## <a name="see-also"></a>См. также раздел

[Класс CStringT](../../atl-mfc-shared/reference/cstringt-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Общие классы ATL и MFC](../../atl-mfc-shared/atl-mfc-shared-classes.md)
