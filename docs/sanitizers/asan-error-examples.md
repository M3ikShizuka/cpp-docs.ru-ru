---
title: Примеры ошибок Аддресссанитизер
description: Описание верхнего уровня ошибок и примеров Аддресссанитизер в Microsoft C/C++.
ms.date: 03/01/2021
helpviewer_keywords:
- ASan error examples
- AddressSanitizer error examples
- Address Sanitizer error examples
- Error examples for AddressSanitizer
ms.openlocfilehash: 6f8036139c48b03fb8300f799fbdf05e5006aa4a
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471333"
---
# <a name="addresssanitizer-error-examples"></a>Примеры ошибок Аддресссанитизер

В этом разделе перечислены подмножество ошибок, поддерживаемых Аддресссанитизер в Microsoft C/C++ (КОМПИЛЯТОРОМ MSVC). Этот список не является исчерпывающим списком ошибок. Он предназначен для отображения нескольких типов ошибок, которые можно увидеть в Аддресссанитизер. В каждой статье мы включили пример кода с инструкциями по построению и снимками экрана отладчика в действии. Они помогут вам научиться использовать функции Аддресссанитизер, поддерживаемые КОМПИЛЯТОРОМ MSVC в коде. Все снимки экрана были созданы с помощью **`devenv.exe /debugexe example.exe`** . Некоторые из этих примеров основаны на примере кода в [наборе тестов LLVM компилятора-RT](https://github.com/llvm/llvm-project/tree/main/compiler-rt/test/asan/TestCases).

## <a name="build-the-error-examples"></a>Построение примеров ошибок

Каждый пример ошибки предоставляет исходный код и инструкции по компиляции для сборки из командной строки. Чтобы построить каждый пример, откройте [командную строку разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts). Создайте папку для примера проекта, а затем сделайте ее текущим каталогом. Затем скопируйте пример кода в исходный файл с соответствующим именем, например *`example1.cpp`* . Следуйте инструкциям по сборке, чтобы создать и запустить инструментированный код в отладчике.

## <a name="errors-with-examples"></a>Ошибки с примерами

- [План `alloc-dealloc-mismatch`](./error-alloc-dealloc-mismatch.md)

- [План `allocation-size-too-big`](./error-allocation-size-too-big.md)

- [План `calloc-overflow`](./error-calloc-overflow.md)

- [План `double-free`](./error-double-free.md)

- [План `dynamic-stack-buffer-overflow`](./error-dynamic-stack-buffer-overflow.md)

- [План `global-overflow`](./error-global-buffer-overflow.md)

- [План `heap-buffer-overflow`](./error-heap-buffer-overflow.md)

- [План `heap-use-after-free`](./error-heap-use-after-free.md)

- [План `invalid-allocation-alignment`](./error-invalid-allocation-alignment.md)

- [План `memcpy-param-overlap`](./error-memcpy-param-overlap.md)

- [План `new-delete-type-mismatch`](./error-new-delete-type-mismatch.md)

- [План `stack-buffer-overflow`](./error-stack-buffer-overflow.md)

- [План `stack-buffer-underflow`](./error-stack-buffer-underflow.md)

- [План `stack-use-after-return`](./error-stack-use-after-return.md)

- [План `stack-use-after-scope`](./error-stack-use-after-scope.md)

- [План `strncat-param-overlap`](./error-strncat-param-overlap.md)

- [План `use-after-poison`](./error-use-after-poison.md)

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)
