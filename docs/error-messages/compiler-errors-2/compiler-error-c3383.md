---
description: 'Дополнительные сведения о: Ошибка компилятора C3383'
title: Ошибка компилятора C3383
ms.date: 11/04/2016
f1_keywords:
- C3383
helpviewer_keywords:
- C3383
ms.assetid: ceb7f725-f417-4dc3-8496-0f413bb76687
ms.openlocfilehash: fb5baf99c6738db1296cf4fb0a509c63d570ad78
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97285595"
---
# <a name="compiler-error-c3383"></a>Ошибка компилятора C3383

operator new при использовании параметра /clr:safe не поддерживается

Строгая типизация в выходном файле, полученном при компиляции с параметром **/clr:safe** , поддается проверке, поэтому указатели не поддерживаются.

Дополнительные сведения см. в следующих разделах:

- [/clr (компиляция среды выполнения)](../../build/reference/clr-common-language-runtime-compilation.md)

- [Общие вопросы использования Visual C++ для 64-разрядных систем](../../build/common-visual-cpp-64-bit-migration-issues.md)

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3383:

```cpp
// C3383.cpp
// compile with: /clr:safe
int main() {
   char* pCharArray = new char[256];  // C3383
}
```
