---
description: 'Дополнительные сведения: _WAIT_CHILD, _WAIT_GRANDCHILD'
title: _WAIT_CHILD, _WAIT_GRANDCHILD
ms.date: 11/04/2016
f1_keywords:
- _WAIT_GRANDCHILD
- WAIT_CHILD
- WAIT_GRANDCHILD
- _WAIT_CHILD
helpviewer_keywords:
- WAIT_CHILD constant
- WAIT_GRANDCHILD constant
- _WAIT_CHILD constant
- _WAIT_GRANDCHILD constant
ms.assetid: 7acd96fa-d118-4339-bb00-e5afaf286945
ms.openlocfilehash: b14586232258f635b428b6c197213782591c8af1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97181661"
---
# <a name="_wait_child-_wait_grandchild"></a>_WAIT_CHILD, _WAIT_GRANDCHILD

## <a name="syntax"></a>Синтаксис

```
#include <process.h>
```

## <a name="remarks"></a>Remarks

Функция `_cwait` может использоваться любым процессом для ожидания любого другого процесса (если известен его идентификатор). Аргумент действия может принимать одно из следующих значений:

|Константа|Значение|
|--------------|-------------|
|`_WAIT_CHILD`|Вызывающий процесс ожидает завершения указанного нового процесса.|
|`_WAIT_GRANDCHILD`|Вызывающий процесс ожидает завершения указанного нового процесса и всех процессов, созданных этим новым процессом.|

## <a name="see-also"></a>См. также раздел

[_cwait](../c-runtime-library/reference/cwait.md)<br/>
[Глобальные константы](../c-runtime-library/global-constants.md)
