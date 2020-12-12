---
description: 'Дополнительные сведения о: Ошибка компилятора C3839'
title: Ошибка компилятора C3839
ms.date: 11/04/2016
f1_keywords:
- C3839
helpviewer_keywords:
- C3839
ms.assetid: 0957faff-1e9f-439b-876b-85bd8d2c578d
ms.openlocfilehash: 8b34cdd7f09bea924d3e184f7ea639c3f8210ed5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97180803"
---
# <a name="compiler-error-c3839"></a>Ошибка компилятора C3839

нельзя изменять выравнивание в управляемом типе или типе WinRT

Выравнивание переменных в управляемых или среда выполнения Windows типах управляется средой CLR или среда выполнения Windows и не может быть изменено с помощью [выравнивания](../../cpp/align-cpp.md).

Следующий пример приводит к возникновению ошибки C3839:

```cpp
// C3839a.cpp
// compile with: /clr
ref class C
{
public:
   __declspec(align(32)) int m_j; // C3839
};

int main()
{
}
```
