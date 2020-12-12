---
description: 'Дополнительные сведения: ошибка средства оценки выражений CXX0064'
title: Ошибка вычислителя выражений CXX0064
ms.date: 11/04/2016
f1_keywords:
- CXX0064
helpviewer_keywords:
- CAN0064
- CXX0064
ms.assetid: aa509e71-0616-41ca-a94e-6c376b041e57
ms.openlocfilehash: 58356a48fc52ee479c92cf5d65494763c3fc4adb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97173198"
---
# <a name="expression-evaluator-error-cxx0064"></a>Ошибка вычислителя выражений CXX0064

не удается задать точку останова для привязанной виртуальной функции члена

Точка останова была задана для виртуальной функции-члена с помощью указателя на объект, например:

```
pClass->vfunc( int );
```

Точку останова можно задать для виртуальной функции, введя класс, например:

```
Class::vfunc( int );
```

Эта ошибка идентична CAN0064.
