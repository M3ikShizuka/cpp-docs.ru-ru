---
description: 'Дополнительные сведения о: Ошибка компилятора C2696'
title: Ошибка компилятора C2696
ms.date: 11/04/2016
f1_keywords:
- C2696
helpviewer_keywords:
- C2696
ms.assetid: 6c6eb7df-1230-4346-9a73-abf14c20785d
ms.openlocfilehash: 2d4a798258ba6f9bb467c4da32e75860b96874e1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97326619"
---
# <a name="compiler-error-c2696"></a>Ошибка компилятора C2696

Невозможно создать временный объект управляемого типа "тип"

**`const`** В неуправляемой программе компилятор вызывает конструктор и создает временный объект в стеке. Однако управляемый класс никогда не может быть создан в стеке.

C2696 доступен только при использовании устаревшего параметра компилятора **/clr: oldSyntax**.
