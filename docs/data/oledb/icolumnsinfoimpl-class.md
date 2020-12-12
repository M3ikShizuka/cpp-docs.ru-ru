---
description: 'Дополнительные сведения о: IColumnsInfoImpl Class'
title: Класс IColumnsInfoImpl
ms.date: 11/04/2016
f1_keywords:
- ATL.IColumnsInfoImpl<T>
- ATL::IColumnsInfoImpl
- IColumnsInfoImpl
- ATL.IColumnsInfoImpl
- ATL::IColumnsInfoImpl<T>
- ATL::IColumnsInfoImpl::GetColumnInfo
- ATL.IColumnsInfoImpl.GetColumnInfo
- ATL::IColumnsInfoImpl<T>::GetColumnInfo
- IColumnsInfoImpl::GetColumnInfo
- IColumnsInfoImpl<T>::GetColumnInfo
- IColumnsInfoImpl.GetColumnInfo
- IColumnsInfoImpl<T>::MapColumnIDs
- MapColumnIDs
- ATL::IColumnsInfoImpl::MapColumnIDs
- IColumnsInfoImpl.MapColumnIDs
- ATL::IColumnsInfoImpl<T>::MapColumnIDs
- IColumnsInfoImpl::MapColumnIDs
- ATL.IColumnsInfoImpl<T>.MapColumnIDs
- ATL.IColumnsInfoImpl.MapColumnIDs
helpviewer_keywords:
- IColumnsInfoImpl class
- GetColumnInfo method
- MapColumnIDs method
ms.assetid: ba74c1c5-2eda-4452-8b57-84919fa0d066
ms.openlocfilehash: 9f6586f4d0315904ea16baf5aa1837bc43107602
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97317627"
---
# <a name="icolumnsinfoimpl-class"></a>Класс IColumnsInfoImpl

Предоставляет реализацию интерфейса [IColumnsInfo](/previous-versions/windows/desktop/ms724541(v=vs.85)) .

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
class ATL_NO_VTABLE IColumnsInfoImpl :
   public IColumnsInfo,
   public CDBIDOps
```

### <a name="parameters"></a>Параметры

*T*<br/>
Класс, производный от `IColumnsInfoImpl` .

## <a name="requirements"></a>Требования

**Заголовок:** atldb.h

## <a name="members"></a>Элементы

### <a name="methods"></a>Методы

| Имя | Описание |
|-|-|
|[GetColumnInfo](#getcolumninfo)|Возвращает метаданные столбца, требуемые большинством объектов-получателей.|
|[мапколумнидс](#mapcolumnids)|Возвращает массив порядковых номеров столбцов в наборе данных, заданных указанными идентификаторами столбца.|

## <a name="remarks"></a>Комментарии

Обязательный интерфейс для наборов строк и команд. Чтобы изменить поведение `IColumnsInfo` реализации поставщика, необходимо изменить карту столбцов поставщика.

## <a name="icolumnsinfoimplgetcolumninfo"></a><a name="getcolumninfo"></a> IColumnsInfoImpl:: GetColumnInfo

Возвращает метаданные столбца, требуемые большинством объектов-получателей.

### <a name="syntax"></a>Синтаксис

```cpp
STDMETHOD (GetColumnInfo)(DBORDINAL* pcColumns,
   DBCOLUMNINFO** prgInfo,
   OLECHAR** ppStringsBuffer);
```

#### <a name="parameters"></a>Параметры

См. раздел [IColumnsInfo:: GetColumnInfo](/previous-versions/windows/desktop/ms722704\(v=vs.85\)) в *справочнике программиста OLE DB*.

## <a name="icolumnsinfoimplmapcolumnids"></a><a name="mapcolumnids"></a> IColumnsInfoImpl:: Мапколумнидс

Возвращает массив порядковых номеров столбцов в наборе данных, заданных указанными идентификаторами столбца.

### <a name="syntax"></a>Синтаксис

```cpp
STDMETHOD (MapColumnIDs)(DBORDINAL cColumnIDs,
   const DBID rgColumnIDs[],
   DBORDINAL rgColumns[]);
```

#### <a name="parameters"></a>Параметры

См. раздел [IColumnsInfo:: мапколумнидс](/previous-versions/windows/desktop/ms714200(v=vs.85)) в *справочнике программиста OLE DB*.

## <a name="see-also"></a>См. также раздел

[Шаблоны поставщика OLE DB](../../data/oledb/ole-db-provider-templates-cpp.md)<br/>
[Архитектура шаблона поставщика OLE DB](../../data/oledb/ole-db-provider-template-architecture.md)
