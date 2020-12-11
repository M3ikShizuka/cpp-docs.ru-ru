---
description: 'Дополнительные сведения: глобальные переменные ATL'
title: Глобальные переменные ATL
ms.date: 12/06/2017
f1_keywords:
- ATLBASE/_pAtlModule
helpviewer_keywords:
- global variables, ATL
- _pAtlModule
ms.assetid: e881a319-99ca-4f5d-8a0b-34b3dcd0f37f
ms.openlocfilehash: 8d0544651e32f5e569973466af8ce04af1433766
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97158781"
---
# <a name="atl-global-variables"></a>Глобальные переменные ATL

## <a name="_patlmodule"></a>_pAtlModule

Глобальная переменная, в которой хранится указатель на текущий модуль.

```cpp
__declspec(selectany) CAtlModule * _pAtlModule
```

### <a name="remarks"></a>Комментарии

Методы в этой глобальной переменной можно использовать для предоставления функциональных возможностей, которые класс (теперь устарел) CComModule, предоставленный в Visual C++ 6,0.

### <a name="example"></a>Пример

```cpp
LONG lLocks = _pAtlModule->GetLockCount();
```

### <a name="requirements"></a>Требования

**Заголовок:** atlbase. h
