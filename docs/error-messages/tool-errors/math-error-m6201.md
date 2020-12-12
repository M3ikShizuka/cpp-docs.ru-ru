---
description: 'Дополнительные сведения: Math Error M6201'
title: Математическая ошибка M6201
ms.date: 11/04/2016
f1_keywords:
- M6201
helpviewer_keywords:
- M6201
ms.assetid: 4041c331-d9aa-4dd4-b565-7dbe0218538c
ms.openlocfilehash: 03588b7eed580b95cb263f6e4d71f5a793f4d392
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97244320"
---
# <a name="math-error-m6201"></a>Математическая ошибка M6201

"функция": ошибка _DOMAIN

Аргумент для данной функции находился вне домена допустимых входных значений для этой функции.

## <a name="example"></a>Пример

```
result = sqrt(-1.0)   // C statement
result = SQRT(-1.0)   !  FORTRAN statement
```

Эта ошибка вызывает `_matherr` функцию с именем функции, ее аргументами и типом ошибки. Можно переписать функцию, `_matherr` чтобы настроить обработку определенных математических ошибок с плавающей запятой во время выполнения.
