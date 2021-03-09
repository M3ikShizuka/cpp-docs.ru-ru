---
title: 'Ошибка: используйте-After-подозрительные'
description: Примеры исходного кода и снимки экрана динамической отладки для использования после ошибок подозрительных сообщений.
ms.date: 03/02/2021
f1_keywords:
- use-after-poison
helpviewer_keywords:
- use-after-poison error
- AddressSanitizer error use-after-poison
ms.openlocfilehash: 0175b79df493dc60c19d78f045ba1829dc0b6b27
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471213"
---
# <a name="error-use-after-poison"></a>Ошибка `use-after-poison` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: использование неповрежденной памяти

Разработчик может вручную завредоносную память для настройки отладки.

## <a name="example"></a>Пример

```cpp
// example1.cpp
// use-after-poison error
#include <stdlib.h>

extern "C" void __asan_poison_memory_region(void *, size_t);

int main(int argc, char **argv) {
    char *x = new char[16];
    x[10] = 0;
    __asan_poison_memory_region(x, 16);

    int res = x[argc * 10];              // Boom!
 
    delete [] x;
    return res;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example1.cpp /fsanitize=address /Zi
devenv /debugexe example1.exe
```

### <a name="resulting-error"></a>Итоговая ошибка

:::image type="content" source="media/use-after-poison-example-1.png" alt-text="Снимок экрана отладчика, отображающий ошибку USE-AFTER-подозрительный в примере 1.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
