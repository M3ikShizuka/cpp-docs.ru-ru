---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4662'
title: Предупреждение компилятора (уровень 1) C4662
ms.date: 11/04/2016
f1_keywords:
- C4662
helpviewer_keywords:
- C4662
ms.assetid: 7efda273-d04a-47b7-ad65-ff1ff94b5ffc
ms.openlocfilehash: 60de9a5f5f4a70fc80eff5322a4757571efd5902
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97318771"
---
# <a name="compiler-warning-level-1-c4662"></a>Предупреждение компилятора (уровень 1) C4662

явное создание экземпляра: для класса-шаблона "идентификатор1" нет определения, из которого можно взять специализацию "идентификатор2"

Указанный класс-шаблон был объявлен, но не определен.

## <a name="example"></a>Пример

```cpp
// C4662.cpp
// compile with: /W1 /LD
template<class T, int i> class MyClass; // no definition
template MyClass< int, 1>;              // C4662
```
