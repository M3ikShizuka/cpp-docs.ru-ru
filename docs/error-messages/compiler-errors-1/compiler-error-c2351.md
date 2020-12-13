---
description: 'Дополнительные сведения о: Ошибка компилятора C2351'
title: Ошибка компилятора C2351
ms.date: 11/04/2016
f1_keywords:
- C2351
helpviewer_keywords:
- C2351
ms.assetid: 5439ccf6-66f6-4859-964c-c73f5eddfc1b
ms.openlocfilehash: ae8cf10cff4a345ee067519d250210f72e6690f8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97145487"
---
# <a name="compiler-error-c2351"></a>Ошибка компилятора C2351

устаревший синтаксис инициализации конструктора C++

В списке инициализации нового стиля для конструктора необходимо явно присвоить имя каждому прямому базовому классу, даже если он является единственным базовым классом.

Следующий пример приводит к возникновению ошибки C2351:

```cpp
// C2351.cpp
// compile with: /c
class B {
public:
   B() : () {}   // C2351
   B() {}   // OK
};
```
