---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4247'
title: Предупреждение средств компоновщика LNK4247
ms.date: 11/04/2016
f1_keywords:
- LNK4247
helpviewer_keywords:
- LNK4247
ms.assetid: 085d7fdf-9eaf-4641-8473-6eaadd073c7b
ms.openlocfilehash: 88cd04e345b798b6927c3a5297380f1eeb3c5f5c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97241187"
---
# <a name="linker-tools-warning-lnk4247"></a>Предупреждение средств компоновщика LNK4247

точка входа "decorated_function_name" уже имеет атрибут потока; атрибут "Attribute" проигнорирован

Также указана точка входа, указанная с параметром [/Entry (символ точки входа)](../../build/reference/entry-entry-point-symbol.md), но [/CLRTHREADATTRIBUTE (Установка атрибута потока CLR)](../../build/reference/clrthreadattribute-set-clr-thread-attribute.md) и с другой потоковой моделью.

Компоновщик проигнорировал значение, указанное с помощью/КЛРСРЕАДАТТРИБУТЕ.

Чтобы устранить это предупреждение, сделайте следующее:

- Удалите/CLRTHREADATTRIBUTE из сборки.

- Удалите атрибут из файла исходного кода.

- Удалите атрибут из Source и/CLRTHREADATTRIBUTE из сборки и примите модель потоков CLR по умолчанию.

- Измените значение, передаваемое в/CLRTHREADATTRIBUTE, таким, что оно соглашается с атрибутом в источнике.

- Измените атрибут в источнике, так что он соглашается со значением, переданным в/КЛРСРЕАДАТТРИБУТЕ..

Следующий пример приводит к возникновению ошибки LNK4247

```cpp
// LNK4247.cpp
// compile with: /clr /c
// post-build command: link /CLRTHREADATTRIBUTE:STA LNK4247.obj /entry:functionTitle /SUBSYSTEM:Console
[System::MTAThreadAttribute]
void functionTitle (){}
```
