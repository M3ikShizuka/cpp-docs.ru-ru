---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4138'
title: Предупреждение компилятора (уровень 1) C4138
ms.date: 11/04/2016
f1_keywords:
- C4138
helpviewer_keywords:
- C4138
ms.assetid: 65ebf929-bba0-4237-923b-c1b66adfe17d
ms.openlocfilehash: 68789c7300944c7435431688ff147f40cd4cadb0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97278029"
---
# <a name="compiler-warning-level-1-c4138"></a>Предупреждение компилятора (уровень 1) C4138

"*/" найден вне комментария

Закрывающему разделителю комментария не предшествует разделитель, открывающий комментарий. Компилятор предполагает пробел между звездочкой ( <strong>\*</strong> ) и косой чертой (/).

## <a name="example"></a>Пример

```cpp
// C4138a.cpp
// compile with: /W1
int */*comment*/ptr;   // C4138 Ambiguous first delimiter causes warning
int main()
{
}
```

Это предупреждение может быть вызвано попыткой создать вложенный комментарий.

Чтобы устранить это предупреждение, раскомментируйте код, содержащий комментарии, поместите его в блок **#if/#endif** и задайте для управляющего выражения значение нуль:

```cpp
// C4138b.cpp
// compile with: /W1
#if 0
int my_variable;   /* Declaration currently not needed */
#endif
int main()
{
}
```
