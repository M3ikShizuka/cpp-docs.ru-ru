---
title: 'Ошибка: динамическое содержимое буфера — переполнение'
description: Примеры исходного кода и снимки экрана динамической отладки для ошибок выделения.
ms.date: 03/02/2021
f1_keywords:
- dynamic-stack-buffer-overflow
helpviewer_keywords:
- dynamic-stack-buffer-overflow error
- AddressSanitizer error dynamic-stack-buffer-overflow
ms.openlocfilehash: 4ccf8c9bbab7eb14cac80f0f1d3f9478fc035f8b
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471252"
---
# <a name="error-dynamic-stack-buffer-overflow"></a>Ошибка `dynamic-stack-buffer-overflow` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: динамическое стек-buffer-переполнение

В этом примере показана ошибка, полученная в результате доступа к буферу за пределами границ объекта, выделенного в стеке.

## <a name="example---alloca-overflow-right"></a>Пример с `alloca` переполнением (справа)

```cpp
// example1.cpp
// dynamic-stack-buffer-overflow error
#include <malloc.h>

__declspec(noinline)
void foo(int index, int len) {

    volatile char *str = (volatile char *)_alloca(len);

    //    reinterpret_cast<long>(str) & 31L;

    str[index] = '1'; // Boom !
}

int main(int argc, char **argv) {

    foo(33, 10);
    return 0;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example1.cpp /fsanitize=address /Zi
devenv /debugexe example1.exe
```

### <a name="resulting-error"></a>Итоговая ошибка

:::image type="content" source="media/dynamic-stack-buffer-overflow-example-1.png" alt-text="Снимок экрана отладчика, отображающий ошибку переполнения динамического стека в примере 1.":::

## <a name="example---alloca-overflow-left"></a>Пример: `alloca` переполнение (слева)

```cpp
// example2.cpp
// dynamic-stack-buffer-overflow error
#include <malloc.h>

__declspec(noinline)
void foo(int index, int len) {

    volatile char *str = (volatile char *)_alloca(len);

    str[index] = '1';  // Boom!
}

int main(int argc, char **argv) {
    foo(-1, 10);
    return 0;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example2.cpp /fsanitize=address /Zi
devenv /debugexe example2.exe
```

### <a name="resulting-error---alloca-overflow-left"></a>Итоговая ошибка- `alloca` переполнение (слева)

:::image type="content" source="media/dynamic-stack-buffer-overflow-example-2.png" alt-text="Снимок экрана отладчика, отображающий ошибку переполнения динамического стека в примере 2.":::

## <a name="example---several-calls-to-alloca"></a>Пример. несколько вызовов `alloca`

```cpp
// example3.cpp
// dynamic-stack-buffer-overflow error
#include <stdio.h>
#include <stdlib.h>
#include <malloc.h>

#define SIZE 7
extern void nothing();
int x=13,*aa,*bb,y=0;
int fail = 0;
int tmp;

int main()
{
    int* cc;
    int i;
    int k = 17;
    __try {
        tmp = k;
        aa = (int*)_alloca(SIZE * sizeof(int));
        if (((int)aa) & 0x3)
            fail = 1;
        for (i = 0; i < SIZE; i++) {
            aa[i] = x + 1 + i;
        }
        bb = (int*)_alloca(x * sizeof(int));
        if (((int)bb) & 0x3)
            fail = 1;

        for (i = 0; i < x; i++) {
            bb[i] = 7;
            bb[i] = bb[i] + i;
        }
        {
            int s = 112728283;
            int ar[8];
            for (i = 0; i < 8; i++)
                ar[i] = s * 17 * i;
        }

        cc = (int*)_alloca(x);
        if (((int)cc) & 0x3)
            fail = 1;

        cc[0] = 0;
        cc[1] = 1;
        cc[2] = 2;
        cc[3] = 3;             // <--- Boom!
        for (i = 0; i < x; i++)
            if (bb[i] != (7 + i))
                fail = 1;
        if (tmp != k)
            fail = 1;
        if (fail) {
            printf("fail\n");
            exit(7);
        }
        printf("%d\n", (*cc) / y);
        printf("fail\n");
        exit(7);
    }
    __except (1)
    {
        for (i = 0; i < SIZE; i++)
            if (aa[i] != (x + i + 1))
                fail = 1;
        if (fail) {
            printf("fail\n");
            exit(7);
        }
        printf("pass\n");
        exit(0);
    }
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example3.cpp /fsanitize=address /Zi
devenv /debugexe example3.exe
```

### <a name="resulting-error---several-calls-to-alloca"></a>Итоговая ошибка — несколько вызовов метода Alloc

:::image type="content" source="media/dynamic-stack-buffer-overflow-example-3.png" alt-text="Снимок экрана отладчика, отображающий ошибку переполнения динамического стека в примере 3.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
