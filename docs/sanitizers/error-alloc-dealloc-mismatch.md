---
title: 'Ошибка: несоответствие выделения и девыделения'
description: Примеры исходного кода и снимки экрана отладки в реальном времени для ошибок несоответствия развыделения.
ms.date: 03/02/2021
f1_keywords:
- alloc-dealloc-mismatch
helpviewer_keywords:
- alloc-dealloc-mismatch error
- AddressSanitizer error alloc-dealloc-mismatch
ms.openlocfilehash: 150809d28631d5d194363e3cb5525163bf7a5e88
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471267"
---
# <a name="error-alloc-dealloc-mismatch"></a>Ошибка `alloc-dealloc-mismatch` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: несоответствие между API выделения и освобождения

`alloc` / `dealloc` Функция несоответствия в аддресссанитизер по умолчанию отключена для Windows. Чтобы включить его, запустите `set ASAN_OPTIONS=alloc_dealloc_mismatch=1` перед запуском программы. Эта переменная среды проверяется во время выполнения для сообщения об ошибках `malloc` / `delete` , `new` / `free` и `new` / `delete[]` .

## <a name="example"></a>Пример

```cpp
// example1.cpp
// alloc-dealloc-mismatch error
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char* argv[]) {

    if (argc != 2) return -1;

    switch (atoi(argv[1])) {

    case 1:
        delete[](new int[10]);
        break;
    case 2:
        delete (new int[10]);      // Boom!
        break;
    default:
        printf("arguments: 1: no error 2: runtime error\n");
        return -1;
    }

    return 0;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example1.cpp /fsanitize=address /Zi
set ASAN_OPTIONS=alloc_dealloc_mismatch=1
devenv /debugexe example1.exe 2
```

### <a name="resulting-error"></a>Итоговая ошибка

:::image type="content" source="media/alloc-dealloc-mismatch-example-1.png" alt-text="Снимок экрана отладчика, отображающий ошибку несоответствия выделения, в примере 1.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
