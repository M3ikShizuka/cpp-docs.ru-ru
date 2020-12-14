---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4580'
title: Предупреждение компилятора (уровень 3) C4580
ms.date: 11/04/2016
f1_keywords:
- C4580
helpviewer_keywords:
- C4580
ms.assetid: fef6e8e0-0d6a-44fa-b22a-2fe7ba2ef379
ms.openlocfilehash: 0bda682526081023c9208d548023f7c8b7316db9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97294721"
---
# <a name="compiler-warning-level-3-c4580"></a>Предупреждение компилятора (уровень 3) C4580

использовать [attribute] не рекомендуется; вместо этого в качестве базового класса укажите System::Attribute или Platform::Metadata

[[Attribute](../../windows/attributes/attribute.md)] больше не является предпочтительным синтаксисом для создания определяемых пользователем атрибутов. Для получения дополнительной информации см. [User-Defined Attributes](../../extensions/user-defined-attributes-cpp-component-extensions.md). Для кода CLR атрибуты должны быть производными от `System::Attribute`. Для кода среды выполнения Windows атрибуты должны быть производными от `Platform::Metadata`.

## <a name="example"></a>Пример

В следующем примере показано возникновение ошибки C3454 и приводятся сведения по ее устранению.

```cpp
// C4580.cpp
// compile with: /W3 /c /clr
[attribute]   // C4580
public ref class Attr {
public:
   int m_t;
};

public ref class Attr2 : System::Attribute {
public:
   int m_t;
};
```
