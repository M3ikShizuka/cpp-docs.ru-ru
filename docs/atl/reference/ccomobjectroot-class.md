---
description: 'Дополнительные сведения о: CComObjectRoot Class'
title: Класс CComObjectRoot
ms.date: 11/04/2016
f1_keywords:
- CComObjectRoot
- atlcom/ATL::CComObjectRoot
helpviewer_keywords:
- CComObjectRoot class
ms.assetid: f8797c38-6e73-4f67-85c2-71654cffa8eb
ms.openlocfilehash: 924b85ee7ed6e17eb44e753ad16f57251bb189ba
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97142471"
---
# <a name="ccomobjectroot-class"></a>Класс CComObjectRoot

Это определение типа [CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md) преобразованный в потоковой модели сервера по умолчанию.

## <a name="syntax"></a>Синтаксис

```
typedef CComObjectRootEx<CComObjectThreadModel> CComObjectRoot;
```

## <a name="remarks"></a>Remarks

`CComObjectRoot` — Это **`typedef`** [CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md) преобразованный в потоковой модели сервера по умолчанию. Таким же [ккомобжектсреадмодел](atl-typedefs.md#ccomobjectthreadmodel) будет ссылаться либо на [ккомсинглесреадмодел](../../atl/reference/ccomsinglethreadmodel-class.md) , либо на [ккоммултисреадмодел](../../atl/reference/ccommultithreadmodel-class.md).

`CComObjectRootEx` обрабатывает управление счетчиком ссылок на объекты для неагрегированных и агрегированных объектов. Он содержит счетчик ссылок на объекты, если объект не выполняет статистическую обработку, и содержит указатель на внешнюю неизвестную функцию, если выполняется статистическая обработка объекта. Для агрегированных объектов `CComObjectRootEx` методы можно использовать для обработки сбоя внутреннего объекта, а также для защиты внешнего объекта от удаления при освобождении внутренних интерфейсов или при удалении внутреннего объекта.

## <a name="requirements"></a>Требования

**Заголовок:** атлком. h

## <a name="see-also"></a>См. также раздел

[Класс CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md)<br/>
[Класс CComAggObject](../../atl/reference/ccomaggobject-class.md)<br/>
[Класс CComObject](../../atl/reference/ccomobject-class.md)<br/>
[Класс CComPolyObject](../../atl/reference/ccompolyobject-class.md)<br/>
[Общие сведения о классах](../../atl/atl-class-overview.md)
