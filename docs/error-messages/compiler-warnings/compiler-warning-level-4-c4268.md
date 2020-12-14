---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4268'
title: Предупреждение компилятора (уровень 4) C4268
ms.date: 11/04/2016
f1_keywords:
- C4268
helpviewer_keywords:
- C4268
ms.assetid: d0511e80-904f-4ee1-b4d7-39b5c0bd8234
ms.openlocfilehash: 50e4a2afd577653fa14ae5d663f2b00fa95670b5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97294669"
---
# <a name="compiler-warning-level-4-c4268"></a>Предупреждение компилятора (уровень 4) C4268

"идентификатор": статические/глобальные данные, инициализированные с помощью конструктора по умолчанию, созданного компилятором, заполняют объект нулями

**`const`** Глобальный или статический экземпляр нетривиального класса инициализируется с помощью созданного компилятором конструктора по умолчанию.

## <a name="example"></a>Пример

```cpp
// C4268.cpp
// compile with: /c /LD /W4
class X {
public:
   int m_data;
};

const X x1;   // C4268
```

Так как этот экземпляр класса является **`const`** , значение `m_data` не может быть изменено.
