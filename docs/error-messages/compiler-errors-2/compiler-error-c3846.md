---
description: 'Дополнительные сведения о: Ошибка компилятора C3846'
title: Ошибка компилятора C3846
ms.date: 11/04/2016
f1_keywords:
- C3846
helpviewer_keywords:
- C3846
ms.assetid: c470f8a5-106b-4efb-b8dc-e1319e04130f
ms.openlocfilehash: 13c9cb7a9dde3710cac31d8ee79fb148f8ff67bb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97255396"
---
# <a name="compiler-error-c3846"></a>Ошибка компилятора C3846

"символ": невозможно импортировать символ из "Assembly2": AS "Symbol" уже был импортирован из другой сборки "сборка Assembly1"

Не удалось импортировать символ из сборки, на которую указывает ссылка, так как она была ранее импортирована из упоминаемой сборки.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3846:

```cpp
// C3846a.cpp
// compile with: /LD /clr
public ref struct G
{
};
```

Затем скомпилируйте следующий код:

```cpp
// C3846b.cpp
// compile with: /clr
#using "c3846a.dll"
#using "c3846a.obj"   // C3846

int main()
{
}
```
