---
title: 'Ошибка: стек — использование-After-Return'
description: Примеры исходного кода и снимки экрана динамической отладки для использования стека после ошибок возврата.
ms.date: 03/02/2021
f1_keywords:
- stack-use-after-return
helpviewer_keywords:
- stack-use-after-return error
- AddressSanitizer error stack-use-after-return
ms.openlocfilehash: 37d950b0c3b4da880524c0c5825d86d6feec9654
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471216"
---
# <a name="error-stack-use-after-return"></a>Ошибка `stack-use-after-return` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: использование памяти стека после возврата

Эта проверка требует создания кода, активированного дополнительным параметром компилятора, [`/fsanitize-address-use-after-return`](../build/reference/fsanitize.md) и путем установки переменной среды `ASAN_OPTIONS=detect_stack_use_after_return=1` .

Эта проверка может существенно замедлить работу приложения. Рассмотрим [Clang сводку](https://github.com/google/sanitizers/wiki/AddressSanitizerUseAfterReturn) алгоритма, который поддерживает использование после возврата, и более высокие затраты на производительность.

> [!IMPORTANT]
> При создании объектного файла с помощью дополнительного параметра компилятора **`/fsanitize-address-use-after-return`** код, создаваемый компилятором, принимает решение о том, как выделить кадр стека. Если переменной среды `ASAN_OPTIONS` не присвоено значение `detect_stack_use_after_return` , код по-прежнему будет медленнее, чем [`/fsanitize=address`](../build/reference/fsanitize.md) сам по себе. Это происходит медленнее, так как по-прежнему возникают дополнительные издержки из некоторых кадров стека, которые выделяют пространство для частей кадра с помощью `alloca()` . Рекомендуется удалить эти файловые файлы по завершении обработки ошибок «использовать после возврата».

## <a name="example---simple-c"></a>Пример — Simple C

```cpp
// example1.cpp
// stack-use-after-return error
char* x;

void foo() {
    char stack_buffer[42];
    x = &stack_buffer[13];
}

int main() {

    foo();
    *x = 42; // Boom!

    return 0;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example1.cpp /fsanitize=address /fsanitize-address-use-after-return /Zi
set ASAN_OPTIONS=detect_stack_use_after_return=1
devenv /debugexe example1.exe
```

### <a name="resulting-error---simple-c"></a>Итоговая ошибка-Simple C

:::image type="content" source="media/stack-use-after-return-example-1.png" alt-text="Снимок экрана отладчика, отображающего ошибку стека-After-return в примере 1.":::

## <a name="example---c-and-templates"></a>Пример — C++ и шаблоны

```cpp
// example2.cpp
// stack-use-after-return error
#include <stdlib.h>

enum ReadOrWrite { Read = 0, Write = 1 };

struct S32 {
    char x[32];
};

template<class T>
T* LeakStack() {
    T t[100];
    static volatile T* x;
    x = &t[0];
    return (T*)x;
}

template<class T>
void StackUseAfterReturn(int Idx, ReadOrWrite w) {
    static T sink;
    T* t = LeakStack<T>();
    if (w)
        t[100 + Idx] = T();
    else
        sink = t[100 + Idx];
}

int main(int argc, char* argv[]) {

    if (argc != 2) return 1;
    int kind = atoi(argv[1]);

    switch (kind) {
    case 1: StackUseAfterReturn<char>(0, Read); break;
    case 2: StackUseAfterReturn<S32>(0, Write); break;
    }
    return 0;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example2.cpp /fsanitize=address /fsanitize-address-use-after-return /Zi
set ASAN_OPTIONS=detect_stack_use_after_return=1
devenv /debugexe example2.exe 1
```

### <a name="resulting-error---c-and-templates"></a>Результирующая Ошибка — C++ и шаблоны

:::image type="content" source="media/stack-use-after-return-example-2.png" alt-text="Снимок экрана отладчика, отображающего ошибку стека-After-return в примере 2.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
