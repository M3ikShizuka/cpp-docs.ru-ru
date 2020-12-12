---
description: 'Дополнительные сведения о: Ижетдатасаурцеимпл Class'
title: Класс IGetDataSourceImpl
ms.date: 11/04/2016
f1_keywords:
- IGetDataSourceImpl
- ATL.IGetDataSourceImpl<T>
- ATL.IGetDataSourceImpl
- ATL::IGetDataSourceImpl
- ATL::IGetDataSourceImpl<T>
- GetDataSource
- IGetDataSourceImpl.GetDataSource
- IGetDataSourceImpl::GetDataSource
helpviewer_keywords:
- IGetDataSourceImpl class
- GetDataSource method
ms.assetid: d63f3178-d663-4f01-8c09-8aab2dd6805a
ms.openlocfilehash: 24cf83b7eb799882f1c7da42854899bcf46fddf2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97287272"
---
# <a name="igetdatasourceimpl-class"></a>Класс IGetDataSourceImpl

Предоставляет реализацию объекта [ижетдатасаурце](/previous-versions/windows/desktop/ms709721(v=vs.85)) .

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
class ATL_NO_VTABLE IGetDataSourceImpl : public IGetDataSource
```

### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IGetDataSourceImpl` .

## <a name="requirements"></a>Требования

**Заголовок:** atldb.h

## <a name="members"></a>Элементы

### <a name="interface-methods"></a>Методы интерфейса

| Имя | Описание |
|-|-|
|[GetDataSource](#getdatasource)|Возвращает указатель интерфейса на объекте источника данных, который создал сеанс.|

## <a name="remarks"></a>Комментарии

Это обязательный интерфейс в сеансе для получения указателя интерфейса на объект источника данных.

## <a name="igetdatasourceimplgetdatasource"></a><a name="getdatasource"></a> Ижетдатасаурцеимпл:: DataSource

Возвращает указатель интерфейса на объекте источника данных, который создал сеанс.

### <a name="syntax"></a>Синтаксис

```cpp
STDMETHOD(GetDataSource)(REFIID riid,
   IUnknown ** ppDataSource);
```

#### <a name="parameters"></a>Параметры

См. раздел [ижетдатасаурце:: DataSource](/previous-versions/windows/desktop/ms725443(v=vs.85)) в *справочнике программиста OLE DB*.

### <a name="remarks"></a>Комментарии

Полезно, если необходимо получить доступ к свойствам в объекте источника данных.

## <a name="see-also"></a>См. также раздел

[Шаблоны поставщика OLE DB](../../data/oledb/ole-db-provider-templates-cpp.md)<br/>
[Архитектура шаблона поставщика OLE DB](../../data/oledb/ole-db-provider-template-architecture.md)
