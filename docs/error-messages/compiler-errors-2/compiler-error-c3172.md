---
description: 'Дополнительные сведения о: Ошибка компилятора C3172'
title: Ошибка компилятора C3172
ms.date: 11/04/2016
f1_keywords:
- C3172
helpviewer_keywords:
- C3172
ms.assetid: 1834e2fd-6036-4c33-aff2-b51bc7c99441
ms.openlocfilehash: d8ce88960e725266723c3c37cd9bfbbbd342027b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97242175"
---
# <a name="compiler-error-c3172"></a>Ошибка компилятора C3172

"module_name": невозможно указать другие атрибуты idl_module в проекте

[](../../windows/attributes/idl-module.md) в `dllname` `version` двух файлах при компиляции были обнаружены idl_module атрибуты с одинаковым именем, но разными параметрами или. `idl_module`Для каждой компиляции можно указать только один уникальный атрибут.

Идентичные `idl_module` атрибуты могут быть указаны в нескольких файлах исходного кода.

Например, если `idl_module` были найдены следующие атрибуты:

```cpp
// C3172.cpp
[module(name="MyMod")];
[ idl_module(name="x", dllname="file.dll", version="1.1") ];
int main() {}
```

Затем:

```cpp
// C3172b.cpp
// compile with: C3172.cpp
// C3172 expected
[ idl_module(name="x", dllname="file.dll", version="1.0") ];
```

компилятор создаст C3172 (Обратите внимание на различные значения версии).
