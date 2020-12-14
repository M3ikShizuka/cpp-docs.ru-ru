---
description: 'Дополнительные сведения о: предупреждение компилятора C4956'
title: Предупреждение компилятора C4956
ms.date: 11/04/2016
f1_keywords:
- C4956
helpviewer_keywords:
- C4956
ms.assetid: 9154f2d1-d49f-4e07-90d2-0e9bc028011a
ms.openlocfilehash: 4a92c6329bf4cdd764fd7f419d8011d4dfde0202
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97314845"
---
# <a name="compiler-warning-c4956"></a>Предупреждение компилятора C4956

> "*тип*": этот тип не поддается проверке

## <a name="remarks"></a>Комментарии

Это предупреждение создается, если указано [/clr:safe](../../build/reference/clr-common-language-runtime-compilation.md) , но код содержит тип, не подлежащий проверке. Параметр компилятора **/clr: Сейф** является устаревшим в visual Studio 2015 и не поддерживается в visual Studio 2017.

Дополнительные сведения см. в разделе [чистый и проверяемый код (C++/CLI)](../../dotnet/pure-and-verifiable-code-cpp-cli.md).

Это предупреждение выдается в качестве ошибки, и его можно отключить с помощью прагмы [warning](../../preprocessor/warning.md) или параметра компилятора [/wd](../../build/reference/compiler-option-warning-level.md) .

## <a name="example"></a>Пример

В следующем примере возникает ошибка C4956.

```cpp
// C4956.cpp
// compile with: /clr:safe
int* p;   // C4956
```
