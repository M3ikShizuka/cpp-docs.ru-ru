---
description: 'Дополнительные сведения о: Неустранимая ошибка C1308'
title: Неустранимая ошибка C1308
ms.date: 11/04/2016
f1_keywords:
- C1308
helpviewer_keywords:
- C1308
ms.assetid: 46177997-069e-433a-8e20-93c846d78ffd
ms.openlocfilehash: 9d9b8cee128b9ed830c4ba3651ee609d91d42eac
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97177878"
---
# <a name="fatal-error-c1308"></a>Неустранимая ошибка C1308

Связывание сборок не поддерживается

NETMODULE-файла допускается в качестве входных данных для компоновщика, а сборка — нет. Эта ошибка может возникать при попытке связать сборку, скомпилированную с `/clr:safe` .

Дополнительные сведения см. в разделе [NETMODULE-файлы в качестве входных файлов компоновщика](../../build/reference/netmodule-files-as-linker-input.md).

Следующий пример приводит к возникновению ошибки C1308:

```cpp
// C1308.cpp
// compile with: /clr:safe /LD
public ref class MyClass {
public:
   int i;
};
```

И потом

```cpp
// C1308b.cpp
// compile with: /clr /link C1308b.obj C1308.dll
// C1308 expected
#using "C1308.dll"
int main() {
   MyClass ^ my = gcnew MyClass();
}
```
