---
title: 'Ошибка: глобальный буфер — переполнение'
description: Примеры исходного кода и снимки экрана динамической отладки для ошибок переполнения глобальной переменной.
ms.date: 03/02/2021
f1_keywords:
- global-buffer-overflow
helpviewer_keywords:
- global-buffer-overflow error
- AddressSanitizer error global-buffer-overflow
ms.openlocfilehash: cdc637318c523d43684f938df51030ec803a754b
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471243"
---
# <a name="error-global-buffer-overflow"></a>Ошибка `global-buffer-overflow` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: переполнение глобального буфера

Компилятор создает метаданные для любой переменной в `.data` `.bss` разделах или. Эти переменные имеют языковую область Global или File static. Они выделяются в памяти перед `main()` запуском. Глобальные переменные в языке C обрабатываются значительно иначе, чем в C++. Это различие обусловлено сложными правилами связывания C.

В C глобальная переменная может быть объявлена в нескольких исходных файлах, и каждое определение может иметь разные типы. Компилятор не может просматривать все возможные определения одновременно, но компоновщик может. Для C компоновщик по умолчанию выбирает переменную самого крупного размера из всех различных объявлений.

В C++ глобальный объект выделяется компилятором. Может существовать только одно определение, поэтому размер каждого определения известен во время компиляции.

## <a name="example---globals-in-c-with-multiple-type-definitions"></a>Пример. глобальные значения в C с несколькими определениями типов

```cpp
// file: a.c
int x;
```

```cpp
// file: b.c
char* x;
```

```cpp
// file: c.c
float* x[3];
```

```cpp
// file: example1-main.c
// global-buffer-overflow error

// AddressSanitizer reports a buffer overflow at the first line
// in function main() in all cases, REGARDLESS of the order in 
// which the object files: a.obj, b.obj, and c.obj are linked.
  
double x[5];
 
int main() { 
    int rc = (int) x[5];  // Boom!
    return rc; 
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl a.c b.c c.c example1-main.c /fsanitize=address /Zi
devenv /debugexe example1-main.exe
```

### <a name="resulting-error"></a>Итоговая ошибка

:::image type="content" source="media/global-overflow-example-1.png" alt-text="Снимок экрана отладчика, отображающий ошибку переполнения глобального буфера в примере 1.":::

## <a name="example---simple-function-level-static"></a>Пример — статический уровень функций static

```cpp
// example2.cpp
// global-buffer-overflow error
#include <string.h>

int 
main(int argc, char **argv) {

    static char XXX[10];
    static char YYY[10];
    static char ZZZ[10];

    memset(XXX, 0, 10); memset(YYY, 0, 10); memset(ZZZ, 0, 10);

    int res = YYY[argc * 10];  // Boom!

    res += XXX[argc] + ZZZ[argc];
    return res;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example2.cpp /fsanitize=address /Zi
devenv /debugexe example2.exe
```

### <a name="resulting-error---simple-function-level-static"></a>Итоговая ошибка — статический уровень функции-простой

:::image type="content" source="media/global-overflow-example-2.png" alt-text="Снимок экрана отладчика, отображающий ошибку переполнения глобального буфера в примере 2.":::

## <a name="example---all-global-scopes-in-c"></a>Пример. все глобальные области в C++

```cpp
// example3.cpp
// global-buffer-overflow error

// Run 4 different ways with the choice of one of these options:
//
// -g : Global
// -c : File static
// -f : Function static
// -l : String literal

#include <string.h>

struct C {
    static int array[10];
};

// normal global
int global[10];

// class static
int C::array[10];

int main(int argc, char **argv) {

    int one = argc - 1;

    switch (argv[1][1]) {
    case 'g': return global[one * 11];     //Boom! simple global
    case 'c': return C::array[one * 11];   //Boom! class static
    case 'f':
        static int array[10];
        memset(array, 0, 10);
        return array[one * 11];            //Boom! function static
    case 'l':
        // literal global ptr created by compiler
        const char *str = "0123456789";
        return str[one * 11];              //Boom! .rdata string literal allocated by compiler
    }
    return 0;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example3.cpp /fsanitize=address /Zi
devenv /debugexe example3.exe -l
```

### <a name="resulting-error---all-global-scopes-in-c"></a>Итоговая ошибка-все глобальные области в C++

:::image type="content" source="media/global-overflow-example-3.png" alt-text="Снимок экрана отладчика, отображающий ошибку переполнения глобального буфера в примере 3.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
