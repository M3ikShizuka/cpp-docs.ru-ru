---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4067'
title: Предупреждение компилятора (уровень 1) C4067
ms.date: 11/04/2016
f1_keywords:
- C4067
helpviewer_keywords:
- C4067
ms.assetid: 1d10353e-8cd5-4b01-9184-a06189b965a4
ms.openlocfilehash: b11167ba5648e71be16197ecfb418d92cb5d879a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97267668"
---
# <a name="compiler-warning-level-1-c4067"></a>Предупреждение компилятора (уровень 1) C4067

> непредвиденные токены после директивы препроцессора — ожидается символ новой строки

## <a name="remarks"></a>Комментарии

Компилятор обнаружил и не пропустил лишние символы после директивы препроцессора. Это может быть вызвано непредусмотренными символами, хотя распространенной причиной является изолированная точка с запятой после директивы. Комментарии не вызывают это предупреждение. Параметр компилятора **/Za** включает это предупреждение для дополнительных директив препроцессора, чем значение по умолчанию.

## <a name="example"></a>Пример

```cpp
// C4067a.cpp
// compile with: cl /EHsc /DX /W1 /Za C4067a.cpp
#include <iostream>
#include <string> s     // C4067
#if defined(X);         // C4067
std::string s{"X is defined"};
#else
std::string s{"X is not defined"};
#endif;                 // C4067 only under /Za
int main()
{
    std::cout << s << std::endl;
}
```

Чтобы устранить это предупреждение, удалите ненужные символы или переместите их в блок комментариев. Некоторые предупреждения C4067 могут быть отключены путем удаления параметра компилятора **/Za** .

```cpp
// C4067b.cpp
// compile with: cl /EHsc /DX /W1 C4067b.cpp
#include <iostream>
#include <string>
#if defined(X)
std::string s{"X is defined"};
#else
std::string s{"X is not defined"};
#endif
int main()
{
    std::cout << s << std::endl;
}
```
