---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4078'
title: Предупреждение средств компоновщика LNK4078
ms.date: 11/04/2016
f1_keywords:
- LNK4078
helpviewer_keywords:
- LNK4078
ms.assetid: 5a16796d-6caf-42d9-8f65-b042843eafb8
ms.openlocfilehash: 3fd22316d0775561c18fc2662c2f2ca843e64977
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97210131"
---
# <a name="linker-tools-warning-lnk4078"></a>Предупреждение средств компоновщика LNK4078

Найдено несколько разделов "имя раздела" с разными атрибутами

Ссылка обнаружила несколько разделов с одинаковыми именами, но с разными атрибутами.

Это предупреждение может быть вызвано библиотекой импорта или файлом экспорта, созданным в предыдущей версии LINK или LIB.

Повторно создайте файл и повторно свяжите его.

## <a name="example"></a>Пример

LNK4078 также может быть вызвана критическим изменением: раздел с именем [init_seg](../../preprocessor/init-seg.md) на платформе x86 был доступен для чтения и записи и теперь доступен только для чтения.

Следующий пример приводит к возникновению ошибки LNK4078.

```cpp
// LNK4078.cpp
// compile with: /W1
// LNK4078 expected
#include <stdio.h>
#pragma warning(disable : 4075)
typedef void (__cdecl *PF)(void);
int cxpf = 0;   // number of destructors to call
PF pfx[200];   // pointers to destructors.

struct A { A() {} };

int myexit (PF pf) { return 0; }

#pragma section(".mine$a", read, write)
// try the following line instead
// #pragma section(".mine$a", read)
__declspec(allocate(".mine$a")) int ii = 1;

#pragma section(".mine$z", read, write)
// try the following line instead
// #pragma section(".mine$z", read)
__declspec(allocate(".mine$z")) int i = 1;

#pragma data_seg()
#pragma init_seg(".mine$m", myexit)
A bbbb;
A cccc;
int main() {}
```
