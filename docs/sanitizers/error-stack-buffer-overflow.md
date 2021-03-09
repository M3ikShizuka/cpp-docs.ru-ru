---
title: 'Ошибка: переполнение буфера стека'
description: Примеры исходного кода и снимки экрана динамической отладки для ошибок переполнения буфера стека.
ms.date: 03/02/2021
f1_keywords:
- stack-buffer-overflow
helpviewer_keywords:
- stack-buffer-overflow error
- AddressSanitizer error stack-buffer-overflow
ms.openlocfilehash: 52b4dcf2caad04703b9fa407f0546e94528849c4
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471225"
---
# <a name="error-stack-buffer-overflow"></a>Ошибка `stack-buffer-overflow` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: переполнение буфера стека

Переполнение буфера стека может происходить по-разному в C или C++. Мы предоставляем несколько примеров для этой категории ошибок, которые можно перехватить с помощью простой перекомпиляции.

## <a name="example---stack-buffer-overflow"></a>Пример. переполнение буфера стека

```cpp
// example1.cpp
// stack-buffer-overflow error
#include <string.h>

int main(int argc, char **argv) {
    char x[10];
    memset(x, 0, 10);
    int res = x[argc * 10];  // Boom! Classic stack buffer overflow

    return res;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example1.cpp /fsanitize=address /Zi
devenv /debugexe example1.exe
```

### <a name="resulting-error"></a>Итоговая ошибка

:::image type="content" source="media/stack-buffer-overflow-example-1.png" alt-text="Снимок экрана отладчика, отображающий ошибку переполнения буфера стека в примере 1.":::

## <a name="example---stack-buffer-math"></a>Пример для вычисления размера буфера стека

```cpp
// example2.cpp
// stack-buffer-overflow error
#include <string.h>
#include <stdio.h>
#include <stdlib.h>
#include <assert.h>

int main(int argc, char **argv) {
    assert(argc >= 2);
    int idx = atoi(argv[1]);
    char AAA[10], BBB[10], CCC[10];
    memset(AAA, 0, sizeof(AAA));
    memset(BBB, 0, sizeof(BBB));
    memset(CCC, 0, sizeof(CCC));
    int res = 0;
    char *p = AAA + idx;
    printf("AAA: %p\ny: %p\nz: %p\np: %p\n", AAA, BBB, CCC, p);

    return *(short*)(p) + BBB[argc % 2] + CCC[argc % 2];  // Boom! ... when argument is 9
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example2.cpp /fsanitize=address /Zi
devenv /debugexe example2.exe 9
```

### <a name="resulting-error---stack-buffer-math"></a>Итоговые математические буферы с ошибками

:::image type="content" source="media/stack-buffer-overflow-example-2.png" alt-text="Снимок экрана отладчика, отображающий ошибку переполнения буфера стека в примере 2.":::

## <a name="example---improper-down-cast-on-stack"></a>Пример. неправильное приведение в стеке

```cpp
// example3.cpp
// stack-buffer-overflow error
class Parent {
public:
    int field;
};

class Child : public Parent {
public:
    int extra_field;
};

int main(void) {

    Parent p;
    Child *c = (Child*)&p;  // Boom !
    c->extra_field = 42;

    return 0;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example3.cpp /fsanitize=address /Zi
devenv /debugexe example3.exe
```

### <a name="resulting-error---improper-down-cast-on-stack"></a>Итоговая ошибка — неправильное приведение в стеке

:::image type="content" source="media/stack-buffer-overflow-example-3.png" alt-text="Снимок экрана отладчика, отображающий ошибку переполнения буфера стека в примере 3.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
