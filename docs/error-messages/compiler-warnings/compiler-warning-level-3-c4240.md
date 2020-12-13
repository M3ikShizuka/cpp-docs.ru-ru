---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4240'
title: Предупреждение компилятора (уровень 3) C4240
ms.date: 11/04/2016
f1_keywords:
- C4240
helpviewer_keywords:
- C4240
ms.assetid: a2657cdb-18e1-493f-882b-4e10c0bca71d
ms.openlocfilehash: 95e704b6ad91ff77c4def0b4fa1fe8fad002e5ae
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97344202"
---
# <a name="compiler-warning-level-3-c4240"></a>Предупреждение компилятора (уровень 3) C4240

использовано нестандартное расширение: доступ к "className" теперь определен как "спецификатор доступа", ранее он был определен как "спецификатор доступа"

В режиме совместимости с ANSI ([/Za](../../build/reference/za-ze-disable-language-extensions.md)) нельзя изменить доступ к вложенному классу. В разделе расширения Майкрософт по умолчанию (/Ze) можно с помощью этого предупреждения.

## <a name="example"></a>Пример

```cpp
// C4240.cpp
// compile with: /W3
class X
{
private:
   class N;
public:
   class N
   {   // C4240
   };
};

int main()
{
}
```
