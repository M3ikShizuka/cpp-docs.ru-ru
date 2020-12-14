---
description: 'Дополнительные сведения о: Ошибка компилятора C2865'
title: Ошибка компилятора C2865
ms.date: 11/04/2016
f1_keywords:
- C2865
helpviewer_keywords:
- C2865
ms.assetid: 973eb6a0-c99a-4d25-b3e5-fe0539794d77
ms.openlocfilehash: 0c57fdb120eb147b3877cc834e142ab92f147aaa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97220751"
---
# <a name="compiler-error-c2865"></a>Ошибка компилятора C2865

"функция": недопустимое сравнение для handle_or_pointer

Можно сравнить ссылки на [классы и структуры](../../extensions/classes-and-structs-cpp-component-extensions.md) или управляемые ссылочные типы только для проверки на равенство, чтобы определить, ссылаются ли они на один и тот же объект (= =) или на разные объекты (! =).

Их нельзя сравнить для упорядочения, так как среда выполнения .NET может перемещать управляемые объекты в любое время, изменяя результат теста.
