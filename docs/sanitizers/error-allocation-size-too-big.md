---
title: 'Ошибка: размер выделения-слишком большой'
description: Примеры исходного кода и снимки экрана динамической отладки для ошибок выделения и размера — слишком большие ошибки.
ms.date: 03/02/2021
f1_keywords:
- allocation-size-too-big
helpviewer_keywords:
- allocation-size-too-big error
- AddressSanitizer error allocation-size-too-big
ms.openlocfilehash: 3320064f52a4d41ca556b9525760997f52e1385b
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471174"
---
# <a name="error-allocation-size-too-big"></a>Ошибка `allocation-size-too-big` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: размер выделения-слишком большой

В этом примере показана ошибка, найденная при слишком большом выделении памяти для кучи. Пример, исходя из [набора тестов LLVM компилятора-RT](https://github.com/llvm/llvm-project/tree/main/compiler-rt/test/asan/TestCases).

## <a name="example"></a>Пример

```cpp
// example1.cpp
// allocation-size-too-big error
#include <stdio.h>
#include <malloc.h>
#include <memory.h>

int x = 1000;
int y = 1000;

__declspec(noinline) void bad_function() {

  char* buffer = (char*)malloc(x * y * x * y); //Boom!

  memcpy(buffer, buffer + 8, 8); 
}

int main(int argc, char **argv) {
    bad_function();
    return 0;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example1.cpp /fsanitize=address /Zi
devenv /debugexe example1.exe
```

### <a name="resulting-error"></a>Итоговая ошибка

:::image type="content" source="media/allocation-size-too-big-example-1.png" alt-text="Снимок экрана отладчика, отображающего выделение-размер — слишком большой ошибка в примере 1.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
