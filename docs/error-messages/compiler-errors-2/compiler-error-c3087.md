---
description: 'Дополнительные сведения о: Ошибка компилятора C3087'
title: Ошибка компилятора C3087
ms.date: 11/04/2016
f1_keywords:
- C3087
helpviewer_keywords:
- C3087
ms.assetid: 4f5bdd52-a853-4f02-b160-6868e9190b9d
ms.openlocfilehash: 0700f10711610e09a797c647e0e107a3ef41f115
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97116370"
---
# <a name="compiler-error-c3087"></a>Ошибка компилятора C3087

"именованный_аргумент": вызов атрибута "атрибут" уже инициализирует данный член

Именованный аргумент был указан в том же блоке атрибута, что и неименованный аргумент для того же значения. Укажите только именованный или неименованный аргумент.

## <a name="example"></a>Пример

В следующем примере возникает ошибка C3087:

```cpp
// C3087.cpp
// compile with: /c
[idl_quote("quote1", text="quote2")];   // C3087
[idl_quote(text="quote3")];   // OK
[idl_quote("quote4")];   // OK
```
