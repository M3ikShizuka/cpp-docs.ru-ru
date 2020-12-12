---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK1312'
title: Ошибка средств компоновщика LNK1312
ms.date: 11/04/2016
f1_keywords:
- LNK1312
helpviewer_keywords:
- LNK1312
ms.assetid: 48284abb-d849-43fc-ab53-45aded14fd8a
ms.openlocfilehash: d861b6976f9b065e3a693e916164879a3311d3db
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97193634"
---
# <a name="linker-tools-error-lnk1312"></a>Ошибка средств компоновщика LNK1312

Недопустимый или поврежденный файл: не удалось импортировать сборку

При построении сборки файл, отличный от модуля или сборки, скомпилированного с **параметром/CLR** , был передан параметру компоновщика **/ASSEMBLYMODULE** .  Если объектный файл был передан в **/ASSEMBLYMODULE**, просто передайте объект непосредственно в компоновщик, а не в **/ASSEMBLYMODULE**.

## <a name="examples"></a>Примеры

В следующем примере создается OBJ-файл.

```cpp
// LNK1312.cpp
// compile with: /clr /LD
public ref class A {
public:
   int i;
};
```

Следующий пример приводит к возникновению ошибки LNK1312.

```cpp
// LNK1312_b.cpp
// compile with: /clr /LD /link /assemblymodule:LNK1312.obj
// LNK1312 error expected
public ref class M {};
```
