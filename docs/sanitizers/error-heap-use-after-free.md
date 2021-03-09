---
title: 'Ошибка: куча-использование-после-Free'
description: Примеры исходного кода и снимки экрана динамической отладки для использования кучи после бесплатных ошибок.
ms.date: 03/02/2021
f1_keywords:
- heap-use-after-free
helpviewer_keywords:
- heap-use-after-free error
- AddressSanitizer error heap-use-after-free
ms.openlocfilehash: 86e64537d40a86b1867e9ba16781f10b6ea9b417
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471131"
---
# <a name="error-heap-use-after-free"></a>Ошибка `heap-use-after-free` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: использование освобожденной памяти

Мы покажем три примера, где хранилище в куче можно выделить `malloc` с помощью, `realloc` (C) и `new` (C++), а также с ошибочным использованием `volatile` .

## <a name="example---malloc"></a>Пример — `malloc`

```cpp
// example1.cpp
// heap-use-after-free error
#include <stdlib.h>

int main() {
  char *x = (char*)malloc(10 * sizeof(char));
  free(x);

  // ...

  return x[5];   // Boom!
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example1.cpp /fsanitize=address /Zi
devenv /debugexe example1.exe
```

### <a name="resulting-error"></a>Итоговая ошибка

:::image type="content" source="media/heap-use-after-free-example-1.png" alt-text="Снимок экрана отладчика с отображением кучи — ошибка использования после окончания в примере 1.":::

## <a name="example---operator-new"></a>Пример — `operator new`

```cpp
// example2.cpp
// heap-use-after-free error
#include <windows.h>

int main() {
  char *buffer = new char[42];
  delete [] buffer;

  // ...

  buffer[0] = 42;  // Boom!
  return 0;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example2.cpp /fsanitize=address /Zi
devenv /debugexe example2.exe
```

### <a name="resulting-error---operator-new"></a>Итоговая ошибка-оператор New

:::image type="content" source="media/heap-use-after-free-example-2.png" alt-text="Снимок экрана отладчика, отображающего кучу — используйте ошибку после истечения бесплатного использования в примере 2.":::

## <a name="example---realloc"></a>Пример — `realloc`

```cpp
// example3.cpp
// heap-use-after-free error
#include <malloc.h>

int main() {
  char *buffer = (char*)realloc(0, 42);
  free(buffer);

  // ...

  buffer[0] = 42;  // Boom!
  return 0;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example3.cpp /fsanitize=address /Zi
devenv /debugexe example3.exe
```

### <a name="resulting-error---realloc"></a>Итоговая ошибка-перераспределения

:::image type="content" source="media/heap-use-after-free-example-3.png" alt-text="Снимок экрана отладчика, отображающего кучу — используйте ошибку после истечения бесплатного использования в примере 3.":::

## <a name="example---volatile"></a>Пример — volatile

```cpp
// example4.cpp
// heap-use-after-free error
#include <stdlib.h>

int main() {

  volatile char *x = (char*)malloc(sizeof(char));
  free((void*)x);

      //...

  *x = 42;        // Boom!
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example4.cpp /fsanitize=address /Zi
devenv /debugexe example4.exe
```

### <a name="resulting-error---volatile"></a>Итоговая ошибка-volatile

:::image type="content" source="media/heap-use-after-free-example-4.png" alt-text="Снимок экрана: ошибка отображения отладчика в примере 4.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
