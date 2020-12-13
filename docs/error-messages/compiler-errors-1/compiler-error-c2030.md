---
description: 'Дополнительные сведения о: Ошибка компилятора C2030'
title: Ошибка компилятора C2030
ms.date: 11/04/2016
f1_keywords:
- C2030
helpviewer_keywords:
- C2030
ms.assetid: 5806cead-64df-4eff-92de-52c9a3f5ee62
ms.openlocfilehash: b29996051a87f050e61c94b4134d046f52be6f09
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97175486"
---
# <a name="compiler-error-c2030"></a>Ошибка компилятора C2030

деструктор с модификатором доступа protected private не может быть членом класса, объявленного как sealed

Класс среда выполнения Windows, объявленный как, **`sealed`** не может иметь защищенный закрытый деструктор. Для запечатанных типов допустимы только открытые виртуальные и закрытые невиртуальные деструкторы. Подробные сведения см. в статье [Ref classes and structs (C++/CX)](../../cppcx/ref-classes-and-structs-c-cx.md) (Ссылочные классы и структуры (C++/CX)).

Чтобы устранить эту ошибку, измените тип доступа деструктора.
