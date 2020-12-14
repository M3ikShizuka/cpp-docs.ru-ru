---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK1179'
title: Ошибка средств компоновщика LNK1179
ms.date: 11/04/2016
f1_keywords:
- LNK1179
helpviewer_keywords:
- LNK1179
ms.assetid: 4b1536d7-0d3d-4f29-a9c1-6fa5cf6cb665
ms.openlocfilehash: 691476eeffadece2436518c5249ca523adca51c2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97253446"
---
# <a name="linker-tools-error-lnk1179"></a>Ошибка средств компоновщика LNK1179

Недопустимый или поврежденный файл: дублирующийся COMDAT "имяфайла"

Модуль объекта содержит два или более COMDAT с одним и тем же именем.

Эта ошибка может быть вызвана параметром [/h](../../build/reference/h-restrict-length-of-external-names.md), который ограничивает длину внешних имен и параметром [/Gy](../../build/reference/gy-enable-function-level-linking.md), который упаковывает функции в COMDAT.

## <a name="example"></a>Пример

В следующем коде `function1` и `function2` являются идентичными в первых восьми символах. Компиляция с параметром **/Gy** и **/H8** приводит к ошибке компоновки.

```cpp
void function1(void);
void function2(void);

int main() {
    function1();
    function2();
}

void function1(void) {}
void function2(void) {}
```
