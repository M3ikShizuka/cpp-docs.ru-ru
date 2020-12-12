---
description: 'Дополнительные сведения о: Ошибка компилятора C3457'
title: Ошибка компилятора C3457
ms.date: 11/04/2016
f1_keywords:
- C3457
helpviewer_keywords:
- C3457
ms.assetid: 5c1e366a-fa75-4cca-b9a3-86d4ebe4090e
ms.openlocfilehash: 42e30946c57da585ed1339e49b6081372b141a2c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97113601"
---
# <a name="compiler-error-c3457"></a>Ошибка компилятора C3457

"атрибут": атрибут не поддерживает неименованные аргументы

Исходные атрибуты заметок, в отличие от атрибутов компилятора или пользовательских атрибутов CLR, поддерживают только именованные аргументы.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3457:

```
#include "SourceAnnotations.h"
[vc_attributes::Post( 1 )] int f();   // C3457
[vc_attributes::Post( Valid=vc_attributes::Yes )] int f2();   // OK
```
