---
description: 'Дополнительные сведения о: Катлфилемаппинг Class'
title: Класс Катлфилемаппинг
ms.date: 11/04/2016
f1_keywords:
- CAtlFileMapping
- atlfile/ATL::CAtlFileMapping
helpviewer_keywords:
- CAtlFileMapping class
ms.assetid: 899fc058-e05e-48b5-aca9-340403bb9e26
ms.openlocfilehash: 875979d47ad4cb5b9c59047eff1f50acd35d1251
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97147424"
---
# <a name="catlfilemapping-class"></a>Класс Катлфилемаппинг

Этот класс представляет размещенный в памяти файл, добавляя оператор приведения к методам [катлфилемаппингбасе](../../atl/reference/catlfilemappingbase-class.md).

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```cpp
template <typename T = char>
class CAtlFileMapping : public CAtlFileMappingBase
```

### <a name="parameters"></a>Параметры

*T*<br/>
Тип данных, используемых для оператора приведения.

## <a name="members"></a>Элементы

### <a name="public-operators"></a>Открытые операторы

|Имя|Описание|
|----------|-----------------|
|[Катлфилемаппинг:: operator T *](#operator_t_star)|Разрешает неявное преобразование `CAtlFileMapping` объектов в `T*` .|

## <a name="remarks"></a>Комментарии

Этот класс добавляет один оператор приведения, чтобы разрешить неявное преобразование `CAtlFileMapping` объектов в `T*` . Другие члены предоставляются базовым классом [катлфилемаппингбасе](../../atl/reference/catlfilemappingbase-class.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[катлфилемаппингбасе](../../atl/reference/catlfilemappingbase-class.md)

`CAtlFileMapping`

## <a name="requirements"></a>Требования

**Заголовок:** атлфиле. h

## <a name="catlfilemappingoperator-t"></a><a name="operator_t_star"></a> Катлфилемаппинг:: operator T *

Разрешает неявное преобразование `CAtlFileMapping` объектов в `T*` .

```cpp
operator T*() const throw();
```

### <a name="return-value"></a>Возвращаемое значение

Возвращает `T*` указатель на начало размещенного в памяти файла.

### <a name="remarks"></a>Комментарии

Вызывает метод [катлфилемаппингбасе:: GetData](../../atl/reference/catlfilemappingbase-class.md#getdata) и повторно интерпретирует возвращенный указатель как, `T*` где *T* — это тип, используемый в качестве параметра шаблона этого класса.

## <a name="see-also"></a>См. также раздел

[Класс Катлфилемаппингбасе](../../atl/reference/catlfilemappingbase-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
