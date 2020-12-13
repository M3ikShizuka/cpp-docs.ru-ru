---
description: 'Дополнительные сведения о: Ошибка компилятора C2396'
title: Ошибка компилятора C2396
ms.date: 11/04/2016
f1_keywords:
- C2396
helpviewer_keywords:
- C2396
ms.assetid: 1b515ef6-7af4-400f-b4ed-564313ea15f6
ms.openlocfilehash: 654b812fbd152a6effb60e6f0919f99bf5039a1b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97145396"
---
# <a name="compiler-error-c2396"></a>Ошибка компилятора C2396

"your_type:: оператор'типе" ": допустимое пользовательское преобразование CLR или WinRT функтионнот. Необходимо либо преобразовать из или преобразовать в: 'T ^ ', ' t ^% ', ' t ^& ', где T = ' your_type '

Функция преобразования в управляемом типе или типе среды выполнения Windows не содержала по крайней мере один параметр, тип которого совпадает с типом, содержащим эту функцию преобразования.

В следующем примере показано возникновение ошибки C2396 и приводятся сведения по ее устранению.

```cpp
// C2396.cpp
// compile with: /clr /c

ref struct Y {
   static operator int(char c);   // C2396

   // OK
   static operator int(Y^ hY);
   // or
   static operator Y^(char c);
};
```
