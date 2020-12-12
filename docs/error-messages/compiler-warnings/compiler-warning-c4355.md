---
description: 'Дополнительные сведения о: предупреждение компилятора C4355'
title: Предупреждение компилятора C4355
ms.date: 11/04/2016
f1_keywords:
- C4355
helpviewer_keywords:
- C4355
ms.assetid: b819ecab-8a07-42d7-8fa4-1180d51626c0
ms.openlocfilehash: fd4d38aae7a3728370c89cb2298438dbc0ba616c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97180777"
---
# <a name="compiler-warning-c4355"></a>Предупреждение компилятора C4355

'this': используется в основном списке инициализации членов

**`this`** Указатель допустим только в нестатических функциях-членах. Его нельзя использовать в списке инициализаторов для базового класса.

Конструкторы базового класса и конструкторы членов класса вызываются перед **`this`** конструктором. Фактически вы передали указатель на несконструированный объект другому конструктору. Если другие конструкторы обращаются к членам или вызывают функции членов для этого, результат будет неопределенным. Не следует использовать **`this`** указатель до завершения всей конструкции.

Это предупреждение отключено по умолчанию. Подробнее: [Выключенные по умолчанию предупреждения компилятора](../../preprocessor/compiler-warnings-that-are-off-by-default.md) .

Следующий пример приводит к возникновению ошибки C4355:

```cpp
// C4355.cpp
// compile with: /w14355 /c
#include <tchar.h>

class CDerived;
class CBase {
public:
   CBase(CDerived *derived): m_pDerived(derived) {};
   ~CBase();
   virtual void function() = 0;

   CDerived * m_pDerived;
};

class CDerived : public CBase {
public:
   CDerived() : CBase(this) {};   // C4355 "this" used in derived c'tor
   virtual void function() {};
};

CBase::~CBase() {
   m_pDerived -> function();
}

int main() {
   CDerived myDerived;
}
```
