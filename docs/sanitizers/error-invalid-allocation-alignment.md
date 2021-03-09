---
title: 'Ошибка: недопустимое выравнивание по выделению'
description: Примеры исходного кода и снимки экрана динамической отладки для недопустимых _aligned_mallocных ошибок.
ms.date: 03/02/2021
f1_keywords:
- invalid-allocation-alignment
helpviewer_keywords:
- invalid-allocation-alignment error
- AddressSanitizer error invalid-allocation-alignment
ms.openlocfilehash: 99318b068c2908bbe9eee63bef80c5f3f5e37e75
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471119"
---
# <a name="error-invalid-allocation-alignment"></a>Ошибка `invalid-allocation-alignment` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: недопустимое выравнивание по выделению

[`_aligned_malloc`](../c-runtime-library/reference/aligned-malloc.md)Для выражения выравнивания функция должна иметь степень 2. Мы моделируем "внешний" вычисление некоторого коэффициента выравнивания с помощью неоптимизированной глобальной переменной.

## <a name="example"></a>Пример

```cpp
// example1.cpp
// invalid-allocation-alignment error
#include <Windows.h>

int ExternalAlign = 5;

int main(){

    // this externally calculated alignment of 5 isn't valid.

    void* ptr = _aligned_malloc(8,ExternalAlign); 
    return (ptr == nullptr && errno == EINVAL) ? 0 : -1;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example1.cpp /fsanitize=address /Zi
devenv /debugexe example1.exe
```

### <a name="resulting-error"></a>Итоговая ошибка

:::image type="content" source="media/invalid-allocation-alignment-example-1.png" alt-text="Снимок экрана отладчика, отображающий ошибку выравнивания при выделении, в примере 1.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
