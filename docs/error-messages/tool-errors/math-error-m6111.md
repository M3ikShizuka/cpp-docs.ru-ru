---
description: 'Дополнительные сведения: Math Error M6111'
title: Математическая ошибка M6111
ms.date: 11/04/2016
f1_keywords:
- M6111
helpviewer_keywords:
- M6111
ms.assetid: c0fc13f8-33c8-4e3f-a440-126cc623441b
ms.openlocfilehash: 9bf2d620a0df18752b74aaacd4d2415510407f0f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97244346"
---
# <a name="math-error-m6111"></a>Математическая ошибка M6111

потеря значимости стека

Операция с плавающей запятой привела к незначимости стека на сопроцессоре 8087/287/387 или в эмуляторе.

Эта ошибка часто возникает из-за вызова **`long double`** функции, которая не возвращает значение. Например, следующая ошибка возникает при компиляции и выполнении:

```
long double ld() {};
main ()
{
  ld();
}
```

Программа завершается с кодом выхода 139.
