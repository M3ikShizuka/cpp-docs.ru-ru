---
title: 'Ошибка: куча-буфер — переполнение'
description: Примеры исходного кода и снимки экрана динамической отладки для ошибок переполнения переменных кучи.
ms.date: 03/02/2021
f1_keywords:
- heap-buffer-overflow
helpviewer_keywords:
- heap-buffer-overflow error
- AddressSanitizer error heap-buffer-overflow
ms.openlocfilehash: 7eec8d0fa8c7382a5a4ecea9811298aaaba760a2
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471135"
---
# <a name="error-heap-buffer-overflow"></a>Ошибка `heap-buffer-overflow` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: переполнение буфера кучи

В этом примере показана ошибка, которая возникает, когда доступ к памяти происходит вне границ объекта, выделенного в куче.

## <a name="example---classic-heap-buffer-overflow"></a>Пример — переполнение буфера классической кучи

```cpp
// example1.cpp
// heap-buffer-overflow error
#include <stdlib.h>
#include <string.h>

int main(int argc, char **argv) {

    char *x = (char*)malloc(10 * sizeof(char));
    memset(x, 0, 10);
    int res = x[argc * 10];  // Boom!

    free(x);
    return res;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example1.cpp /fsanitize=address /Zi
devenv /debugexe example1.exe
```

### <a name="resulting-error"></a>Итоговая ошибка

:::image type="content" source="media/heap-buffer-overflow-example-1.png" alt-text="Снимок экрана отладчика с ошибкой переполнения буфера кучи в примере 1.":::

## <a name="example---improper-down-cast"></a>Пример. неправильное приведение

```cpp
// example2.cpp
// heap-buffer-overflow error
class Parent {
public:
    int field;
};

class Child : public Parent {
public:
    int extra_field;
};

int main(void) {
    Parent *p = new Parent;
    Child *c = (Child*)p;  // Intentional error here!
    c->extra_field = 42;

    return 0;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example2.cpp /fsanitize=address /Zi
devenv /debugexe example2.exe
```

### <a name="resulting-error---improper-down-cast"></a>Итоговая ошибка — неправильное приведение

:::image type="content" source="media/heap-buffer-overflow-example-2.png" alt-text="Снимок экрана: ошибка переполнения буфера кучи при отображении отладчика в примере 2.":::

## <a name="example---strncpy-into-heap"></a>Пример. strncpy в кучу

```cpp
// example3.cpp
// heap-buffer-overflow error
#include <string.h>
#include <stdlib.h>

int main(int argc, char **argv) {

    char *hello = (char*)malloc(6);
    strcpy(hello, "hello");

    char *short_buffer = (char*)malloc(9);
    strncpy(short_buffer, hello, 10);  // Boom!

    return short_buffer[8];
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example3.cpp /fsanitize=address /Zi
devenv /debugexe example3.exe
```

### <a name="resulting-error---strncpy-into-heap"></a>Итоговая ошибка — strncpy в кучу

:::image type="content" source="media/heap-buffer-overflow-example-3.png" alt-text="Снимок экрана отладчика, отображающий ошибку переполнения буфера кучи в примере 3.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
