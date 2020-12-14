---
description: 'Дополнительные сведения о: sequenced_policy классе'
title: Класс sequenced_policy
ms.date: 04/18/2019
f1_keywords:
- execution/std::execution::sequenced_policy
ms.openlocfilehash: e4d19e3649e3c768e8efc062baaf735e28a8fc22
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97250417"
---
# <a name="sequenced_policy-class"></a>Класс sequenced_policy

Используется в качестве уникального типа для устранения неоднозначности при перегрузке параллельного алгоритма и требует, чтобы выполнение параллельного алгоритма не было параллельным.

## <a name="syntax"></a>Синтаксис

```cpp
class execution::sequenced_policy;
```

## <a name="remarks"></a>Remarks

При выполнении параллельного алгоритма с `execution::sequenced_policy` политикой, если вызов функции доступа к элементу завершается через неперехваченное исключение, то `terminate()` должно быть вызвано.
