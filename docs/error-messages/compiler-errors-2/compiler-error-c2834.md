---
description: 'Дополнительные сведения о: Ошибка компилятора C2834'
title: Ошибка компилятора C2834
ms.date: 11/04/2016
f1_keywords:
- C2834
helpviewer_keywords:
- C2834
ms.assetid: 28f9f6eb-ab2a-4e64-aaaa-9d14f955de41
ms.openlocfilehash: 6f74853f264af653988ed77ddb9a9c7935f3c542
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97194440"
---
# <a name="compiler-error-c2834"></a>Ошибка компилятора C2834

"operator оператор" должен быть глобально полным

`new`Операторы и `delete` привязаны к классу, где они находятся. Разрешение области нельзя использовать для выбора версии `new` или `delete` из другого класса. Чтобы реализовать несколько форм `new` `delete` оператора OR, создайте версию оператора с дополнительными формальными параметрами.
