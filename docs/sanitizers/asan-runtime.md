---
title: Среда выполнения Аддресссанитизер
description: Техническое описание среды выполнения Аддресссанитизер для Microsoft C/C++.
ms.date: 03/02/2021
helpviewer_keywords:
- AddressSanitizer runtime
- Address Sanitizer runtime
- clang_rt.asan
- Clang runtime
- ASan runtime
ms.openlocfilehash: 6ab27365ba6841dd5314f1eac65abd71b7d4170d
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471179"
---
# <a name="addresssanitizer-runtime"></a>Среда выполнения Аддресссанитизер

Библиотека времени выполнения Аддресссанитизер перехватывает общие функции и операции выделения памяти, чтобы обеспечить проверку доступа к памяти. Существует несколько разных библиотек среды выполнения, поддерживающих различные типы исполняемых файлов, которые может создать компилятор. Компилятор и компоновщик автоматически связывают соответствующие библиотеки среды выполнения при условии, что параметр передается [`/fsanitize=address`](../build/reference/fsanitize.md) во время компиляции. Поведение по умолчанию можно переопределить с помощью **`/NODEFAULTLIB`** параметра во время компоновки. Дополнительные сведения см. в разделе, посвященном [ссылкам](./asan-building.md#linker) в [справочнике по языку аддресссанитизер, сборке и отладке](./asan-building.md).

Ниже приведен список библиотек времени выполнения для связывания со средой выполнения Аддресссанитизер, где *`{arch}`* имеет значение *`i386`* или *`x86_64`* .

> [!NOTE]
> Эти библиотеки сохраняют соглашения Clang для имен архитектуры. Соглашения КОМПИЛЯТОРОМ MSVC обычно представляют собой x86 и x64, а не i386 и x86_64. Они ссылаются на одну и ту же архитектуру.

| CRT, параметр | DLL или EXE | СМ? | Библиотеки двоичных файлов среды выполнения Аддресссанитизер |
|--|--|--|--|
| MT | EXE | NO | *`clang_rt.asan-{arch}`*, *`clang_rt.asan_cxx-{arch}`* |
| MT | DLL | NO | *`clang_rt.asan_dll_thunk-{arch}`* |
| MD | ЛЮБОЙ | NO | *`clang_rt.asan_dynamic-{arch}`*, *`clang_rt.asan_dynamic_runtime_thunk-{arch}`* |
| MT | EXE | YES | *`clang_rt.asan_dbg-{arch}`*, *`clang_rt.asan_dbg_cxx-{arch}`* |
| MT | DLL | YES | *`clang_rt.asan_dbg_dll_thunk-{arch}`* |
| MD | ЛЮБОЙ | YES | *`clang_rt.asan_dbg_dynamic-{arch}`*, *`clang_rt.asan_dbg_dynamic_runtime_thunk-{arch}`* |

При компиляции с `cl /fsanitize=address` компилятор создает инструкции для управления и проверки [теневых байтов](./asan-shadow-bytes.md). Программа использует это инструментирование для проверки доступа к памяти в стеке, в куче или в глобальной области. Компилятор также создает метаданные, описывающие стек и глобальные переменные. Эти метаданные позволяют среде выполнения создавать точную диагностику ошибок: имена функций, строки и столбцы в исходном коде. В сочетании с проверками компилятора и библиотеками времени выполнения можно точно диагностировать множество типов [ошибок безопасности памяти](./asan-error-examples.md) , если они встречаются во время выполнения.

## <a name="function-interception"></a>Перехват функции

Аддресссанитизер достигает перехвата функций с помощью многих методов горячего исправления. Эти методы [лучше документировать в исходном коде](https://github.com/llvm/llvm-project/blob/1a2eaebc09c6a200f93b8beb37130c8b8aab3934/compiler-rt/lib/interception/interception_win.cpp#L11).

Библиотеки среды выполнения перехватывают многие стандартные функции управления памятью и обработки в памяти. Список см. в разделе [аддресссанитизер List of Конст functions](#intercepted_functions). Перехватчики распределения управляют метаданными и теневыми байтами, связанными с каждым вызовом распределения. Каждый раз `malloc` , когда вызывается функция CRT, например или `delete` , перехватчики задают определенные значения в области теневой памяти аддресссанитизер, чтобы указать, доступны ли эти расположения в данный момент и каковы границы выделения. Эти байты с тенью позволяют автоматически создавать компилятором проверки [теневых байтов](./asan-shadow-bytes.md) , чтобы определить, является ли загрузка или хранилище допустимыми.

Перехват не гарантируется. Если пролог функции слишком короткий для `jmp` написания, перехват может завершиться ошибкой. Если происходит сбой перехвата, программа создает исключение `debugbreak` и останавливается. Если вы подключаете отладчик, это приводит к устранению проблемы с перехватом. Если у вас есть эта проблема, [сообщите об ошибке](https://aka.ms/feedback/report?space=62).

> [!NOTE]
> При необходимости пользователи могут попытаться продолжить работу после неудачного перехвата, задав `ASAN_WIN_CONTINUE_ON_INTERCEPTION_FAILURE` для переменной среды любое значение. Продолжение работы после сбоя перехвата может привести к пропуску отчетов об ошибках для этой функции.

## <a name="custom-allocators-and-the-addresssanitizer-runtime"></a>Пользовательские распределителя и среда выполнения Аддресссанитизер

Среда выполнения аддресссанитизер предоставляет перехватчики для распространенных интерфейсов распределителя,, `malloc` / `free` `new` / `delete` , `HeapAlloc` / `HeapFree` (Via `RtlAllocateHeap` / `RtlFreeHeap` ). Многие программы используют пользовательские распределителя по одной из причин или другой, например, любая программа, использующая `dlmalloc` или решение, использующее `std::allocator` интерфейс и `VirtualAlloc()` . Компилятору не удается автоматически добавить вызовы управления теневой памятью в пользовательский распределитель. Ответственность за использование [предоставленного ручного интерфейса](#poisoning). Этот API позволяет этим распределителям правильно работать с существующей средой выполнения Аддресссанитизер и соглашениями о [теневых байтах](./asan-shadow-bytes.md) .

## <a name="manual-addresssanitizer-poisoning-interface"></a><a name="poisoning"></a> Аддресссанитизерный интерфейс для подозрительных сообщений

Интерфейс для интересны прост, но он накладывает ограничения на выравнивание для пользователя. Пользователи могут импортировать эти прототипы путем импорта [`sanitizer/asan_interface.h`](https://github.com/llvm/llvm-project/blob/main/compiler-rt/include/sanitizer/asan_interface.h) . Ниже приведены прототипы функций интерфейса.

```cpp
void __asan_poison_memory_region(void const volatile *addr, size_t size);
void __asan_unpoison_memory_region(void const volatile *addr, size_t size);
```

Для удобства [файл заголовка интерфейса аддресссанитизер](https://github.com/llvm/llvm-project/blob/main/compiler-rt/include/sanitizer/asan_interface.h) предоставляет макросы-оболочки. Эти макросы проверяют, включена ли функция Аддресссанитизер во время компиляции. Они позволяют исходному коду опускать вызовы неповрежденных функций, если они не нужны. Эти макросы следует использовать для непосредственного вызова функций, указанных выше.

```cpp
#define ASAN_POISON_MEMORY_REGION(addr, size)
#define ASAN_UNPOISON_MEMORY_REGION(addr, size)
```

## <a name="alignment-requirements-for-addresssanitizer-poisoning"></a>Требования к выравниванию для подозрительных Аддресссанитизер

Любой ручной запрет на теневые байты должен учитывать требования к выравниванию. При необходимости пользователь должен добавить заполнение, чтобы байты с тенью заканчивались на границе байт в теневой памяти. Каждый бит в теневой памяти Аддресссанитизер кодирует состояние одного байта в памяти приложения. Такая кодировка означает, что общий размер каждого выделения, включая заполнение, должен быть выровнен по 8-байтовой границе. Если требования к выравниванию не удовлетворены, это может привести к неправильным отчетам об ошибках. Неправильные отчеты могут проявляться в виде отсутствующих отчетов (ложных отрицательных результатов) или отчетов о неошибках (ложных положительных результатов).

Сведения о требованиях к выравниванию и потенциальных проблемах см. в приведенных [примерах выравнивания Асан](https://github.com/mcgov/asan_alignment_example). Одна из них — небольшая программа, показывающая, что может быть неверно при скрытии памяти с помощью теневой тени. Второй — пример реализации ручного запрета с помощью `std::allocator` интерфейса.

## <a name="run-time-options"></a>Параметры времени выполнения

Microsoft C/C++ (КОМПИЛЯТОРОМ MSVC) использует среду выполнения на основе [среды выполнения Clang аддресссанитизер из репозитория LLVM-Project](https://github.com/llvm/llvm-project). По этой причине большинство параметров среды выполнения совместно используются двумя версиями. [Полный список общедоступных параметров среды выполнения Clang](https://github.com/google/sanitizers/wiki/SanitizerCommonFlags)см. здесь. В следующих разделах мы рассмотрим некоторые отличия. Если обнаруживаются параметры, которые не работают должным образом, [сообщите об ошибке](https://aka.ms/feedback/report?space=62).

### <a name="unsupported-addresssanitizer-options"></a>Неподдерживаемые параметры Аддресссанитизер

- detect_container_overflow
- unmap_shadow_on_exit

> [!NOTE]
> Параметр среды выполнения Аддресссанитизер `halt_on_error` не работает так, как вы можете ожидать. В библиотеках среды выполнения Clang и КОМПИЛЯТОРОМ MSVC многие типы ошибок считаются **небесперебойными**, включая большинство ошибок повреждения памяти.

Дополнительные сведения см. в разделе [различия с Clang 12,0](./asan.md#differences) .

### <a name="msvc-specific-addresssanitizer-runtime-options"></a>Параметры среды выполнения Аддресссанитизер, относящиеся к КОМПИЛЯТОРОМ MSVC

- `windows_hook_legacy_allocators` Логическое значение, заданное для `true` включения перехвата [`GlobalAlloc`](/windows/win32/api/winbase/nf-winbase-globalalloc) и [`LocalAlloc`](/windows/win32/api/winbase/nf-winbase-localalloc) распределителя.

> [!NOTE]
> `windows_hook_legacy_allocators`При написании этой статьи параметр был недоступен в общедоступной среде выполнения LLVM-Project. В конечном итоге параметр может быть вновь включен в общедоступный проект. Однако это зависит от проверки кода и принятия сообщества.
>
> Параметр `windows_hook_rtl_allocators` , ранее аддресссанитизер в экспериментальном режиме, теперь включен по умолчанию.

## <a name="addresssanitizer-list-of-intercepted-functions-windows"></a><a name="intercepted_functions"></a> Аддресссанитизер список перехваченных функций (Windows)

Функция горячего исправления среды выполнения Аддресссанитизер включает в себя множество функций для включения проверок безопасности памяти во время выполнения. Ниже приведен неисчерпывающий список функций, которые наблюдает за средой выполнения Аддресссанитизер.

### <a name="default-interceptors"></a>Перехватчики по умолчанию

- [`__C_specific_handler` (только x64)](/windows/win32/devnotes/--c-specific-handler2)
- [`_aligned_free`](../c-runtime-library/reference/aligned-free.md)
- [`_aligned_malloc`](../c-runtime-library/reference/aligned-malloc.md)
- [`_aligned_msize`](../c-runtime-library/reference/aligned-msize.md)
- [`_aligned_realloc`](../c-runtime-library/reference/aligned-realloc.md)
- [`_calloc_base`](../c-runtime-library/reference/calloc.md)
- [`_calloc_crt`](../c-runtime-library/reference/calloc.md)
- [`_calloc_dbg` (только среда выполнения отладки)](../c-runtime-library/reference/calloc-dbg.md)
- [`_except_handler3` (только x86)](../c-runtime-library/except-handler3.md)
- [ `_except_handler4` (только x86)](../c-runtime-library/internal-crt-globals-and-functions.md) (недокументированный)
- [`_expand`](../c-runtime-library/reference/expand.md)
- `_expand_base` Недокументированные
- [`_expand_dbg` (только среда выполнения отладки)](../c-runtime-library/reference/expand-dbg.md)
- [`_free_base`](../c-runtime-library/internal-crt-globals-and-functions.md) Недокументированные
- [`_free_dbg` (только среда выполнения отладки)](../c-runtime-library/reference/free-dbg.md)
- [`_malloc_base`](../c-runtime-library/internal-crt-globals-and-functions.md) Недокументированные
- `_malloc_crt` Недокументированные
- [`_malloc_dbg` (только среда выполнения отладки)](../c-runtime-library/reference/malloc-dbg.md)
- [`_msize`](../c-runtime-library/reference/msize.md)
- `_msize_base` Недокументированные
- [`_msize_dbg` (только среда выполнения отладки)](../c-runtime-library/reference/msize-dbg.md)
- [`_realloc_base`](../c-runtime-library/internal-crt-globals-and-functions.md) Недокументированные
- `_realloc_crt` Недокументированные
- [`_realloc_dbg` (только среда выполнения отладки)](../c-runtime-library/reference/realloc-dbg.md)
- [`_recalloc`](../c-runtime-library/reference/recalloc.md)
- `_recalloc_base` Недокументированные
- `_recalloc_crt` Недокументированные
- [`_recalloc_dbg` (только среда выполнения отладки)](../c-runtime-library/reference/recalloc-dbg.md)
- [`_strdup`](../c-runtime-library/reference/strdup-wcsdup-mbsdup.md)
- [`atoi`](../c-runtime-library/reference/atoi-atoi-l-wtoi-wtoi-l.md)
- [`atol`](../c-runtime-library/reference/atoi-atoi-l-wtoi-wtoi-l.md)
- [`calloc`](../c-runtime-library/reference/calloc.md)
- [`CreateThread`](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)
- [`free`](../c-runtime-library/reference/free.md)
- [`frexp`](../c-runtime-library/reference/frexp.md)
- [`longjmp`](../c-runtime-library/reference/longjmp.md)
- [`malloc`](../c-runtime-library/reference/malloc.md)
- [`memchr`](../c-runtime-library/reference/memchr-wmemchr.md)
- [`memcmp`](../c-runtime-library/reference/memcmp-wmemcmp.md)
- [`memcpy`](../c-runtime-library/reference/memcpy-wmemcpy.md)
- [`memmove`](../c-runtime-library/reference/memmove-wmemmove.md)
- [`memset`](../c-runtime-library/reference/memset-wmemset.md)
- [`RaiseException`](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)
- [`realloc`](../c-runtime-library/reference/realloc.md)
- [`RtlAllocateHeap`](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
- [`RtlCreateHeap`](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
- [`RtlDestroyHeap`](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
- [`RtlFreeHeap`](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlfreeheap)
- [`RtlRaiseException`](/windows/win32/api/rtlsupportapi/nf-rtlsupportapi-rtlraiseexception)
- `RtlReAllocateHeap` Недокументированные
- `RtlSizeHeap` Недокументированные
- [`SetUnhandledExceptionFilter`](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)
- [`strcat`](../c-runtime-library/reference/strcat-wcscat-mbscat.md)
- [`strchr`](../c-runtime-library/reference/strchr-wcschr-mbschr-mbschr-l.md)
- [`strcmp`](../c-runtime-library/reference/strcmp-wcscmp-mbscmp.md)
- [`strcpy`](../c-runtime-library/reference/strcpy-wcscpy-mbscpy.md)
- [`strcspn`](../c-runtime-library/reference/strcspn-wcscspn-mbscspn-mbscspn-l.md)
- [`strdup`](../c-runtime-library/reference/strdup-wcsdup.md)
- [`strlen`](../c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l.md)
- [`strncat`](../c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l.md)
- [`strncmp`](../c-runtime-library/reference/strncmp-wcsncmp-mbsncmp-mbsncmp-l.md)
- [`strncpy`](../c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l.md)
- [`strnlen`](../c-runtime-library/reference/strnlen-strnlen-s.md)
- [`strpbrk`](../c-runtime-library/reference/strpbrk-wcspbrk-mbspbrk-mbspbrk-l.md)
- [`strspn`](../c-runtime-library/reference/strspn-wcsspn-mbsspn-mbsspn-l.md)
- [`strstr`](../c-runtime-library/reference/strstr-wcsstr-mbsstr-mbsstr-l.md)
- [`strtok`](../c-runtime-library/reference/strtok-strtok-l-wcstok-wcstok-l-mbstok-mbstok-l.md)
- [`strtol`](../c-runtime-library/reference/strtol-wcstol-strtol-l-wcstol-l.md)
- [`wcslen`](../c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l.md)
- [`wcsnlen`](../c-runtime-library/reference/strnlen-strnlen-s.md)

### <a name="optional-interceptors"></a>Необязательные перехватчики

Перечисленные здесь перехватчики устанавливаются только при включенном параметре среды выполнения Аддресссанитизер. Задайте `windows_hook_legacy_allocators` значение `true` , чтобы включить перехват устаревших распределителя.
`set ASAN_OPTIONS=windows_hook_legacy_allocators=true`

- [`GlobalAlloc`](/windows/win32/api/winbase/nf-winbase-globalalloc)
- [`GlobalFree`](/windows/win32/api/winbase/nf-winbase-GlobalFree)
- [`GlobalHandle`](/windows/win32/api/winbase/nf-winbase-GlobalHandle)
- [`GlobalLock`](/windows/win32/api/winbase/nf-winbase-GlobalLock)
- [`GlobalReAlloc`](/windows/win32/api/winbase/nf-winbase-GlobalReAlloc)
- [`GlobalSize`](/windows/win32/api/winbase/nf-winbase-GlobalSize)
- [`GlobalUnlock`](/windows/win32/api/winbase/nf-winbase-GlobalUnlock)
- [`LocalAlloc`](/windows/win32/api/winbase/nf-winbase-LocalAlloc)
- [`LocalFree`](/windows/win32/api/winbase/nf-winbase-LocalFree)
- [`LocalHandle`](/windows/win32/api/winbase/nf-winbase-LocalHandle)
- [`LocalLock`](/windows/win32/api/winbase/nf-winbase-LocalLock)
- [`LocalReAlloc`](/windows/win32/api/winbase/nf-winbase-LocalReAlloc)
- [`LocalSize`](/windows/win32/api/winbase/nf-winbase-LocalSize)
- [`LocalUnlock`](/windows/win32/api/winbase/nf-winbase-LocalUnlock)

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
