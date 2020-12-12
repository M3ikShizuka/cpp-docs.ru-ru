---
description: Дополнительные сведения о перечислении Асинкресулттипе
title: AsyncResultType - перечисление
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- async/Microsoft::WRL::AsyncResultType
helpviewer_keywords:
- AsyncResultType enumeration
ms.assetid: 4195d234-3f3f-4363-9118-6ad2a7551cf2
ms.openlocfilehash: 431c0cabf98b3636bbae02b2f05a14d11d122740
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97175824"
---
# <a name="asyncresulttype-enumeration"></a>AsyncResultType - перечисление

Указывает тип результата, возвращаемого `GetResults()` методом.

## <a name="syntax"></a>Синтаксис

```cpp
enum AsyncResultType;
```

## <a name="members"></a>Члены

### <a name="values"></a>Значения

|Имя|Описание|
|----------|-----------------|
|`MultipleResults`|Набор из нескольких результатов, которые представляются последовательно между `Start` состоянием и перед `Close()` вызовом.|
|`SingleResult`|Один результат, представленный после `Complete` возникновения события.|

## <a name="requirements"></a>Требования

**Заголовок:** Async. h

**Пространство имен:** Microsoft::WRL

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL](microsoft-wrl-namespace.md)
