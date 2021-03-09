---
title: 'Ошибка: стек-USE-AFTER-Scope'
description: Примеры исходного кода и снимки экрана динамической отладки для использования стека после ошибок области.
ms.date: 02/05/2021
f1_keywords:
- stack-use-after-scope
helpviewer_keywords:
- stack-use-after-scope error
- AddressSanitizer error stack-use-after-scope
ms.openlocfilehash: 2b6e3ada1cc5b76b371e8059e045735b16d4b334
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471110"
---
# <a name="error-stack-use-after-scope"></a>Ошибка `stack-use-after-scope` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: использование памяти стека вне области

Использование адреса стека за пределами лексической области действия переменной времени существования может происходить многими способами в C или C++.

## <a name="example-1---simple-nested-local"></a>Пример 1. простое вложенное локальное

```cpp
// example1.cpp
// stack-use-after-scope error
int *gp;

bool b = true;

int main() {
    if (b) {
        int x[5];
        gp = x+1;
    }
    return *gp;  // Boom!
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example1.cpp /fsanitize=address /Zi
devenv /debugexe example1.exe
```

### <a name="resulting-error---simple-nested-local"></a>Итоговая ошибка — простая вложенная локальная

:::image type="content" source="media/stack-use-after-scope-example-1.png" alt-text="Снимок экрана с отладчиком, отображающий ошибку стека — использование после области действия в примере 1.":::

## <a name="example-2---lambda-capture"></a>Пример 2. запись в лямбда-выражении

```cpp
// example2.cpp
// stack-use-after-scope error
#include <functional>

int main() {
    std::function<int()> f;
    {
        int x = 0;
        f = [&x]() {
            return x;  // Boom!
        };
    }
    return f();  // Boom!
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example2.cpp /fsanitize=address /Zi
devenv /debugexe example2.exe
```

### <a name="resulting-error---lambda-capture"></a>Результирующая ошибка-запись лямбды

:::image type="content" source="media/stack-use-after-scope-example-2.png" alt-text="Снимок экрана с отладчиком, отображающий ошибку стека — использование после области в примере 2.":::

## <a name="example-3---destructor-ordering-with-locals"></a>Пример 3. упорядочение деструкторов с помощью локальных переменных

```cpp
// example3.cpp
// stack-use-after-scope error
#include <stdio.h>

struct IntHolder {
    explicit IntHolder(int* val = 0) : val_(val) { }
    ~IntHolder() {
        printf("Value: %d\n", *val_);  // Bom!
    }
    void set(int* val) { val_ = val; }
    int* get() { return val_; }

    int* val_;
};

int main(int argc, char* argv[]) {
    // It's incorrect to use "x" inside the IntHolder destructor,
    // because the lifetime of "x" ends earlier. Per the C++ standard,
    // local lifetimes end in reverse order of declaration.
    IntHolder holder;
    int x = argc;
    holder.set(&x);
    return 0;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example3.cpp /fsanitize=address /Zi /O1
devenv /debugexe example3.exe
```

### <a name="resulting-error---destructor-ordering"></a>Итоговая ошибка — упорядочение деструкторов

:::image type="content" source="media/stack-use-after-scope-example-3.png" alt-text="Снимок экрана с отладчиком, отображающий ошибку стека — использование после области действия в примере 3.":::

## <a name="example-4---temporaries"></a>Пример 4. долгим сроком

```cpp
// example4.cpp
// stack-use-after-scope error
#include <iostream>

struct A {
    A(const int& v) {
        p = &v;
    }
    void print() {
        std::cout << *p;
    }
    const int* p;
};

void explicit_temp() {
    A a(5);     // the temp for 5 is no longer live;
    a.print();
}

void temp_from_conversion() {
    double v = 5;
    A a(v);     // local v is no longer live.
    a.print();
}

void main() {
    explicit_temp();
    temp_from_conversion(); 
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example4.cpp /EHsc /fsanitize=address /Zi
devenv /debugexe example4.exe
```

### <a name="resulting-error---temporaries"></a>Итоговая ошибка — долгим сроком

:::image type="content" source="media/stack-use-after-scope-example-4.png" alt-text="Снимок экрана с отладчиком, отображающий ошибку стека — использование после области действия в примере 4.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
