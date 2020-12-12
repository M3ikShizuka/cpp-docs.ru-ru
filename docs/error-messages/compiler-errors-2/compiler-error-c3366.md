---
description: 'Дополнительные сведения о: Ошибка компилятора C3366'
title: Ошибка компилятора C3366
ms.date: 11/04/2016
f1_keywords:
- C3366
helpviewer_keywords:
- C3366
ms.assetid: efc55bcf-c16d-43c1-a36f-87a6165fa2a8
ms.openlocfilehash: 922fa882efcaead4df87bbfc104394e12b797955
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97150843"
---
# <a name="compiler-error-c3366"></a>Ошибка компилятора C3366

"переменная": статические данные членов управляемых или Винрттипес должны быть определены в определении класса

Вы попытались сослаться на статический элемент класса WinRT, .NET или на интерфейс вне определения этого класса или интерфейса.

Компилятору требуется полное определение класса (для передачи метаданных после одного прохода), а статические элементы данных должны инициализироваться внутри класса.

Так, в следующем примере возникает ошибка C3366 и показано, как ее исправить.

```cpp
// C3366.cpp
// compile with: /clr /c
ref class X {
   public:
   static int i;   // initialize i here to avoid C3366
};

int X::i = 5;      // C3366
```
