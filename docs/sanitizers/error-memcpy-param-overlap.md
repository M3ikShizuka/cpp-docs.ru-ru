---
title: 'Ошибка: memcpy-param-перекрытие'
description: Примеры исходного кода и снимки экрана динамической отладки для ошибок перекрытия параметров memcpy.
ms.date: 03/02/2021
f1_keywords:
- memcpy-param-overlap
helpviewer_keywords:
- memcpy-param-overlap error
- AddressSanitizer error memcpy-param-overlap
ms.openlocfilehash: 1df0310ab2abb326cf895a72afbdffa7c239d9da
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471240"
---
# <a name="error-memcpy-param-overlap"></a>Ошибка `memcpy-param-overlap` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: memcpy-param-перекрытие

Функция CRT [`memcpy`](../c-runtime-library/reference/memcpy-wmemcpy.md) **не поддерживает** перекрытие памяти. CRT предоставляет альтернативу `memcpy` , который поддерживает перекрытие памяти: [`memmove`](../c-runtime-library/reference/memmove-wmemmove.md) .

Распространенная ошибка состоит в том, чтобы интерпретировать `memmove` как семантически эквивалентную `memcpy` .

## <a name="example"></a>Пример

```cpp
// example1.cpp
// memcpy-param-overlap error
#include <string.h>

__declspec(noinline) void bad_function() {
    char buffer[] = "hello";

    memcpy(buffer, buffer + 1, 5); // BOOM!
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

:::image type="content" source="media/memcpy-param-overlap-example-1.png" alt-text="Снимок экрана отладчика, отображающего ошибку перекрытия memcpy в примере 1.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
