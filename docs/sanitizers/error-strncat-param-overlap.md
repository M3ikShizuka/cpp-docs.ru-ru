---
title: 'Ошибка: strncat-param-перекрытие'
description: Примеры исходного кода и снимки экрана динамической отладки для ошибок перекрытия параметров strcat.
ms.date: 03/02/2021
f1_keywords:
- strncat-param-overlap
helpviewer_keywords:
- strncat-param-overlap error
- AddressSanitizer error strcat-param-overlap
ms.openlocfilehash: 9ae5b6f602d61f26e1c5d3d9eded35d3f587c53e
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471107"
---
# <a name="error-strncat-param-overlap"></a>Ошибка `strncat-param-overlap` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: strncat-param-перекрытие

Код, который перемещает память в перекрывающихся буферах, может привести к возникновению ошибок.

## <a name="example"></a>Пример

В этом примере показано, как Аддресссанитизер может перехватывать ошибки, вызванные перекрытием параметров в функции CRT.

(На основе [ллвм-Прожект/компилер-РТ/Test/Асан/TestCases/стрнкат-оверлап. cpp](https://github.com/llvm/llvm-project/blob/62ec4ac90738a5f2d209ed28c822223e58aaaeb7/compiler-rt/test/asan/TestCases/strncat-overlap.cpp).)

```cpp
// example1.cpp
// strncat-param-overlap error
#include <string.h>

void bad_function() {
    char buffer[] = "hello\0XXX";
    strncat(buffer, buffer + 1, 3); // BOOM
    return;
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

:::image type="content" source="media/strcat-param-overlap-example-1.png" alt-text="Снимок экрана отладчика, отображающего ошибку перекрытия strncat в примере 1.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
