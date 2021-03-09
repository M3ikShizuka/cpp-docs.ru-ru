---
title: 'Ошибка: стек-буфер-недостаточный поток'
description: Примеры исходного кода и снимки экрана динамической отладки для ошибок неточного буфера стека.
ms.date: 03/02/2021
f1_keywords:
- stack-buffer-underflow
helpviewer_keywords:
- stack-buffer-underflow error
- AddressSanitizer error stack-buffer-underflow
ms.openlocfilehash: 78705933378d7880057d9b7fd13a933f73129fcb
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471115"
---
# <a name="error-stack-buffer-underflow"></a>Ошибка `stack-buffer-underflow` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: потеря значимости буфера стека

Эти сообщения об ошибках указывают на доступ к памяти в любом месте перед началом переменной стека.

## <a name="example---local-array-underflow"></a>Пример — потеря значимости локальных массивов

```cpp
// example1.cpp
// stack-buffer-underflow error
#include <stdio.h>

int main() {

    int subscript = -1;
    char buffer[42];
    buffer[subscript] = 42; // Boom!
   
    return 0;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example1.cpp /fsanitize=address /Zi
devenv /debugexe example1.exe
```

### <a name="resulting-error"></a>Итоговая ошибка

:::image type="content" source="media/stack-buffer-underflow-example-1.png" alt-text="Снимок экрана: ошибка неточного буфера стека при отображении кода в примере 1.":::

## <a name="example---stack-underflow-on-thread"></a>Пример. потеря точности стека в потоке

```cpp
// example2.cpp
// stack-buffer-underflow error
#include <windows.h>

DWORD WINAPI thread_proc(void *) {
    int subscript = -1;
    volatile char stack_buffer[42];
    stack_buffer[subscript] = 42;

    return 0;
}

int main() {
    HANDLE thr = CreateThread(NULL, 0, thread_proc, NULL, 0, NULL);

    if (thr == 0) return 0;

    WaitForSingleObject(thr, INFINITE);

    return 0;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example2.cpp /fsanitize=address /Zi
devenv /debugexe example2.exe
```

### <a name="resulting-error----stack-underflow-on-thread"></a>Результирующая потеря значимости стека в потоке

:::image type="content" source="media/stack-buffer-underflow-example-2.png" alt-text="Снимок экрана: ошибка неточного буфера стека при отображении кода в примере 2.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
