---
title: 'Ошибка: двойной свободный'
description: Примеры исходного кода и снимки экрана динамической отладки для ошибок двойного освобождения.
ms.date: 03/02/2021
f1_keywords:
- double-free
helpviewer_keywords:
- double-free error
- AddressSanitizer error double-free
ms.openlocfilehash: 6fb508e581a8c19474311d0406622e6353208433
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471261"
---
# <a name="error-double-free"></a>Ошибка `double-free` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: освобождение памяти при освобождении

В C можно вызывать `free` ошибочно. В C++ можно вызывать `delete` несколько раз. В этих примерах отображаются ошибки с `delete` , `free` и `HeapCreate` .

## <a name="example-c---double-operator-delete"></a>Пример C++-Double `operator delete`

```cpp
// example1.cpp
// double-free error
int main() {

    int *x = new int[42];
    delete [] x;

    // ... some complex body of code

    delete [] x;
    return 0;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example1.cpp /fsanitize=address /Zi
devenv /debugexe example1.exe
```

### <a name="resulting-error---double-operator-delete"></a>Итоговая ошибка-Double `operator delete`

:::image type="content" source="media/double-free-example-1.png" alt-text="Снимок экрана отладчика, отображающего ошибку двойного освобождения в примере 1.":::

## <a name="example-c---double-free"></a>Пример "C" — Double `free`

```cpp
// example2.cpp
// double-free error
#include <stdlib.h>
#include <string.h>

int main(int argc, char** argv) {

    char* x = (char*)malloc(10 * sizeof(char));
    memset(x, 0, 10);
    int res = x[argc];
    free(x);

    // ... some complex body of code

    free(x + argc - 1);  // Boom!
    return res;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example2.cpp /fsanitize=address /Zi
devenv /debugexe example2.exe
```

### <a name="resulting-error---double-free"></a>Итоговая ошибка-Double `free`

:::image type="content" source="media/double-free-example-2.png" alt-text="Снимок экрана отладчика, отображающего ошибку двойного освобождения в примере 2.":::

## <a name="example---windows-heapcreate-double-heapfree"></a>Пример Windows `HeapCreate` Double `HeapFree`

```cpp
// example3.cpp
// double-free error
#include <Windows.h>
#include <stdio.h>

int main() {
    void* newHeap = HeapCreate(0, 0, 0);
    void* newAlloc = HeapAlloc(newHeap, 0, 100);

    HeapFree(newHeap, 0, newAlloc);
    HeapFree(newHeap, 0, newAlloc);
    printf("failure\n");
    return 1;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example3.cpp /fsanitize=address /Zi
devenv /debugexe example3.exe
```

### <a name="resulting-error---windows-heapcreate-double-heapfree"></a>Результирующая ошибка-Windows `HeapCreate` Double `HeapFree`

:::image type="content" source="media/double-free-example-3.png" alt-text="Снимок экрана отладчика, отображающего ошибку двойного освобождения в примере 3.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
