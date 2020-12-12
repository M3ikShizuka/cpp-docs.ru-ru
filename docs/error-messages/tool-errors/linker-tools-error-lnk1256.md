---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK1256'
title: Ошибка средств компоновщика LNK1256
ms.date: 11/04/2016
f1_keywords:
- LNK1256
helpviewer_keywords:
- LNK1256
ms.assetid: 55b64b2b-a56b-436c-a55e-ec9c6dcb050e
ms.openlocfilehash: 33dc240e194d93253f3bbf3a5fcd56722b6634d1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97193803"
---
# <a name="linker-tools-error-lnk1256"></a>Ошибка средств компоновщика LNK1256

Ошибка операции ALINK : причина

Наиболее частая причина LNK1256 — неверный номер версии сборки. Значение 65535 не может быть использовано в любой части номера версии сборки. Допустимый диапазон версий сборки — 0-65534.

LNK1256 может возникнуть в случае, если ALINK не удается найти именованный контейнер ключа. Удалите контейнер ключей и снова добавьте его в CSP строгого имени с помощью [Sn.exe (средство строгих имен)](/dotnet/framework/tools/sn-exe-strong-name-tool).

Еще одна возможная причина ошибки LNK1256 — несовпадение версий компоновщика и Alink.dll. Это может быть вызвано поврежденной установкой Visual Studio. Используйте **программы и компоненты** на панели управления Windows для восстановления или переустановки Visual Studio.

Следующий пример приводит к возникновению ошибки LNK1256:

```cpp
// LNK1256.cpp
// compile with: /clr /LD
// LNK1256 expected
[assembly:System::Reflection::AssemblyVersionAttribute("1.0.65535")];
public class CMyClass {
public:
   int value;
};
```
