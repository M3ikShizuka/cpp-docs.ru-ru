---
description: 'Дополнительные сведения о: parallel_policy классе'
title: Класс parallel_policy
ms.date: 04/18/2019
f1_keywords:
- execution/std::execution::parallel_policy
ms.openlocfilehash: 1cead0bcc44256bf7d41d061d592849a7411b057
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340805"
---
# <a name="parallel_policy-class"></a>Класс parallel_policy

Используется в качестве уникального типа для устранения неоднозначности при перегрузке параллельного алгоритма и указывает, что выполнение параллельного алгоритма может быть параллельным.

## <a name="syntax"></a>Синтаксис

```cpp
class execution::parallel_policy;
```

## <a name="remarks"></a>Remarks

При выполнении параллельного алгоритма с `execution::parallel_policy` политикой, если вызов функции доступа к элементу завершается через неперехваченное исключение, то `terminate()` должно быть вызвано.
