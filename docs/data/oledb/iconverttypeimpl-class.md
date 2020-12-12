---
description: 'Дополнительные сведения о: Иконверттипеимпл Class'
title: Класс IConvertTypeImpl
ms.date: 11/04/2016
f1_keywords:
- ATL.IConvertTypeImpl<T>
- IConvertTypeImpl
- ATL.IConvertTypeImpl
- ATL::IConvertTypeImpl
- ATL::IConvertTypeImpl<T>
- IConvertTypeImpl.CanConvert
- CanConvert
- IConvertTypeImpl::CanConvert
helpviewer_keywords:
- IConvertTypeImpl class
- CanConvert method
ms.assetid: 7f81e79e-7d3f-4cbe-b93c-d632a94b15f6
ms.openlocfilehash: 5ac0e70432dbb81bd3f8aa30fd2adb9cb9e3fc30
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97317572"
---
# <a name="iconverttypeimpl-class"></a>Класс IConvertTypeImpl

Предоставляет реализацию интерфейса [Интерфейс IConvertType](/previous-versions/windows/desktop/ms715926(v=vs.85)) .

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
class ATL_NO_VTABLE IConvertTypeImpl
   : public IConvertType, public CConvertHelper
```

### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IConvertTypeImpl` .

## <a name="requirements"></a>Требования

**Заголовок:** atldb.h

## <a name="members"></a>Элементы

### <a name="interface-methods"></a>Методы интерфейса

| Имя | Описание |
|-|-|
|[канконверт](#canconvert)|Предоставляет сведения о доступности преобразований типов в команде или в наборе строк.|

## <a name="remarks"></a>Комментарии

Этот интерфейс является обязательным для команд, наборов строк и наборов строк индекса. `IConvertTypeImpl` реализует интерфейс путем делегирования объекту преобразования, предоставленному OLE DB.

## <a name="iconverttypeimplcanconvert"></a><a name="canconvert"></a> Иконверттипеимпл:: Канконверт

Предоставляет сведения о доступности преобразований типов в команде или в наборе строк.

### <a name="syntax"></a>Синтаксис

```cpp
STDMETHOD(CanConvert)(DBTYPE wFromType,
   DBTYPE wToType,
   DBCONVERTFLAGS dwConvertFlags);
```

#### <a name="parameters"></a>Параметры

См. раздел [Интерфейс IConvertType:: канконверт](/previous-versions/windows/desktop/ms711224(v=vs.85)) в *справочнике программиста OLE DB*.

### <a name="remarks"></a>Комментарии

Использует OLE DB преобразования данных в `MSADC.DLL` .

## <a name="see-also"></a>См. также раздел

[Шаблоны поставщика OLE DB](../../data/oledb/ole-db-provider-templates-cpp.md)<br/>
[Архитектура шаблона поставщика OLE DB](../../data/oledb/ole-db-provider-template-architecture.md)
