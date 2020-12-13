---
description: 'Дополнительные сведения о: parallel_unsequenced_policy классе'
title: Класс parallel_unsequenced_policy
ms.date: 04/18/2019
f1_keywords:
- execution/std::execution::parallel_unsequenced_policy
ms.openlocfilehash: e39edc0979bf1374bc6092dbadb032811180f668
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340792"
---
# <a name="parallel_unsequenced_policy-class"></a>Класс parallel_unsequenced_policy

Используется в качестве уникального типа для устранения неоднозначности при перегрузке параллельного алгоритма и указывает, что выполнение параллельного алгоритма может быть параллельным и векторным.

## <a name="syntax"></a>Синтаксис

```cpp
class execution::parallel_unsequenced_policy;
```

## <a name="remarks"></a>Remarks

При выполнении параллельного алгоритма с `execution::parallel_unsequenced_policy` политикой, если вызов функции доступа к элементу завершается через неперехваченное исключение, то `terminate()` должно быть вызвано.
