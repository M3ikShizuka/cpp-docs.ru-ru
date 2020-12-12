---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4944'
title: Предупреждение компилятора (уровень 1) C4944
ms.date: 11/04/2016
f1_keywords:
- C4944
helpviewer_keywords:
- C4944
ms.assetid: e2905eb1-2e3b-4fab-a48b-c0cae0fd997f
ms.openlocfilehash: 8feff4072bec649761e14dbd74a74e7023f810cd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97328015"
---
# <a name="compiler-warning-level-1-c4944"></a>Предупреждение компилятора (уровень 1) C4944

"символ": не удается импортировать символ из "сборка1": "символ" уже существует в текущей области видимости

Символ был определен в файле исходного кода, а затем оператор #using предоставил ссылку на сборку, в которой также был определен этот символ. Символ в сборке пропускается.

## <a name="examples"></a>Примеры

В приведенном ниже примере создается компонент типа ClassA.

```csharp
// C4944.cs
// compile with: /target:library
// C# source code to create a dll
public class ClassA {
   public int i;
}
```

Следующий пример приводит к возникновению предупреждения C4944:

```cpp
// C4944b.cpp
// compile with: /clr /W1
class ClassA {
public:
   int u;
};

#using "C4944.dll"   // C4944 ClassA also defined C4944.dll

int main() {
   ClassA * x = new ClassA();
   x->u = 9;
   System::Console::WriteLine(x->u);
}
```
