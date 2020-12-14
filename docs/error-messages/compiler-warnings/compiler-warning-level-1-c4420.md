---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4420'
title: Предупреждение компилятора (уровень 1) C4420
ms.date: 11/04/2016
f1_keywords:
- C4420
helpviewer_keywords:
- C4420
ms.assetid: 44a37754-7ddd-4764-a5f7-d33e05c20091
ms.openlocfilehash: 2a92d7296bf5c38655182e5c0dd2c200d0ccf42d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97311075"
---
# <a name="compiler-warning-level-1-c4420"></a>Предупреждение компилятора (уровень 1) C4420

"оператор": оператор недоступен, вместо него используется оператор "operator"; Проверка во время выполнения может быть нарушена

Это предупреждение создается при использовании [/рткв](../../build/reference/rtc-run-time-error-checks.md) (Проверка создания или удаления вектора) и при отсутствии векторной формы. В этом случае используется невекторная форма.

Чтобы/рткв правильно работать, компилятор должен всегда вызывать векторную форму [нового](../../cpp/new-operator-cpp.md) / [удаления](../../cpp/delete-operator-cpp.md) , если использовался синтаксис Vector.
