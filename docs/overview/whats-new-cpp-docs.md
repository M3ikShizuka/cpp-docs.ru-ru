---
title: Новое в документации по C++
description: Новые документы и обновления документации для компилятора Microsoft C/C++, ATL/MFC, среды выполнения C и стандартных библиотек.
ms.date: 02/17/2021
ms.openlocfilehash: ad626dc598cd17de091801b2c313b7339db4cbc7
ms.sourcegitcommit: 5efc34c2b98d4d0d3e41aec38b213f062c19d078
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101844537"
---
# <a name="microsoft-c-docs-whats-new-for-visual-studio-168"></a>Документация по Microsoft C++: Новые возможности Visual Studio 16.8

В этой статье перечислены основные изменения, внесенные в документацию по Visual Studio 16.8. 

Сведения о новых возможностях в Visual Studio см. в статье [Новые возможности C++ в Visual Studio](what-s-new-for-visual-cpp-in-visual-studio.md).

Сведения об актуальном состоянии соответствия C++ см. в разделе [Улучшение соответствия C++ в Visual Studio](cpp-conformance-improvements.md)

## <a name="c-language"></a>Язык C

### <a name="new-articles"></a>Новые статьи

- [Ключевое слово `_Noreturn` и макрос `noreturn` (C11)](../c-language/noreturn.md)
- [Ключевое слово _Static_assert и макрос static_assert (C11)](../c-language/static-assert-c.md)

### <a name="updated-articles"></a>Обновленные статьи

- [Синтаксический анализ аргументов командной строки C](../c-language/parsing-c-command-line-arguments.md) — задокументированы исключения из правил для аргументов C
- [Квалификаторы типов](../c-language/type-qualifiers.md) — добавлен `restrict`
- [Операторы присваивания C](../c-language/c-assignment-operators.md) — обновлена лексическая грамматика для C17
- [Ключевые слова C](../c-language/c-keywords.md) — обновлена лексическая грамматика для C17
- [Лексическая грамматика C](../c-language/lexical-grammar.md) — обновлена лексическая грамматика для C17
- [Сводка объявлений](../c-language/summary-of-declarations.md) — обновлена лексическая грамматика для C17
- [Сводка выражений](../c-language/summary-of-expressions.md) — обновлена лексическая грамматика для C17
- [Объявления перечисления C](../c-language/c-enumeration-declarations.md)исправлена лексическая грамматика
- [Сводка инструкций C](../c-language/summary-of-statements.md) — обновлена для ключевых слов `__leave`, `__try`

## <a name="c-runtime-library"></a>Библиотека среды выполнения C

### <a name="new-articles"></a>Новые статьи

- [Математические символы универсального типа](../c-runtime-library/tgmath.md)

### <a name="updated-articles"></a>Обновленные статьи

- [`qsort`](../c-runtime-library/reference/qsort.md) — добавлено замечание о стабильности
- [`_cwait`](../c-runtime-library/reference/cwait.md) —исправлен пример кода
- [Обзор семейства функций](../c-runtime-library/function-family-overviews.md) — добавлены операторы `new` и `delete`
- [`round, roundf, roundl`](../c-runtime-library/reference/round-roundf-roundl.md) —уточнен пример кода округления
- [Совместимость](../c-runtime-library/compatibility.md) — добавлены примечания о согласованности C99
- [`realloc`](../c-runtime-library/reference/realloc.md) — добавлены примечания о согласованности C99
- [Функции библиотеки CRT](../c-runtime-library/crt-library-features.md) — добавлены примечания о согласованности C99
- [`assert Macro, _assert, _wassert`](../c-runtime-library/reference/assert-macro-assert-wassert.md) — уточнено поведение утверждений
- [`vsnprintf_s, _vsnprintf_s, _vsnprintf_s_l, _vsnwprintf_s, _vsnwprintf_s_l`](../c-runtime-library/reference/vsnprintf-s-vsnprintf-s-vsnprintf-s-l-vsnwprintf-s-vsnwprintf-s-l.md) — уточнены возвращаемые значения
- [`setlocale, _wsetlocale`](../c-runtime-library/reference/setlocale-wsetlocale.md) — добавлена информация о поддержке UTF-8 средой выполнения C

## <a name="cc-preprocessor-reference"></a>Справочник по препроцессору в C/C++

### <a name="updated-articles"></a>Обновленные статьи

- [Предварительно заданные макросы](../preprocessor/predefined-macros.md) — обновлено до заметок о выпуске 16.8, а также документация по поддержке C11/C17 `/std` и установке пакета SDK
- [Обзор нового препроцессора MSVC](../preprocessor/preprocessor-experimental-overview.md) — обновлено содержимое о препроцессоре

## <a name="code-quality"></a>Качество кода

### <a name="new-articles"></a>Новые статьи

- [C33001](../code-quality/c33001.md) — анализ кода VC — добавлены новые правила в 16.8
- [C33004](../code-quality/c33004.md) — анализ кода VC — добавлены новые правила в 16.8
- [C33005](../code-quality/c33005.md) — анализ кода VC — добавлены новые правила в 16.8
- [C33010](../code-quality/c33010.md) — анализ кода VC — добавлены новые правила в 16.8
- [C33011](../code-quality/c33011.md) — анализ кода VC — добавлены новые правила в 16.8
- [C33020](../code-quality/c33020.md) — анализ кода VC — добавлены новые правила в 16.8
- [C33022](../code-quality/c33022.md) — анализ кода VC — добавлены новые правила в 16.8

### <a name="updated-articles"></a>Обновленные статьи

- [`C6262`](../code-quality/c6262.md) — устранена проблема 20 с cpp-docs.zh-tw
- [`C26497 USE_CONSTEXPR_FOR_FUNCTION`](../code-quality/c26497.md) — добавлен пример в C26497
- [`C26496 USE_CONST_FOR_VARIABLE`](../code-quality/c26496.md) — добавлен пример в C26496
- [`C26495 MEMBER_UNINIT`](../code-quality/c26495.md) — обновлены примеры и ссылки в C26495
- [`C26483 STATIC_INDEX_OUT_OF_RANGE`](../code-quality/c26483.md) — добавлен пример в C26483
- [`C26462 USE_CONST_POINTER_FOR_VARIABLE`](../code-quality/c26462.md) — добавлены описание и пример в C26462
- [`C26461 USE_CONST_POINTER_ARGUMENTS:`](../code-quality/c26461.md) — добавлены описание и пример в C26461
- [`C26460 USE_CONST_REFERENCE_ARGUMENTS`](../code-quality/c26460.md) — добавлены описание и пример в C26460
- [`C26440 DECLARE_NOEXCEPT`](../code-quality/c26440.md) — добавлены пример и ссылка на Core Guidelines в C26440
- [`C26439 SPECIAL_NOEXCEPT`](../code-quality/c26439.md) — добавлены пример и ссылка на Core Guidelines в C26439
- [`C26436 NEED_VIRTUAL_DTOR`](../code-quality/c26436.md) — добавлены пример и ссылка на Core Guidelines в C26436
- [`C26408 NO_MALLOC_FREE`](../code-quality/c26408.md) — добавлены пример и ссылка на Core Guidelines в C26408
- [`C26401 DONT_DELETE_NON_OWNER`](../code-quality/c26401.md) — добавлены пример и ссылка на Core Guidelines в C26401
- [`C26494 VAR_USE_BEFORE_INIT`](../code-quality/c26494.md) — добавлен пример в C26494
- [`C26493 NO_CSTYLE_CAST`](../code-quality/c26493.md) — добавлен пример в C26493
- [`C26492 NO_CONST_CAST`](../code-quality/c26492.md) — добавлен пример в C26492
- [`C26490 NO_REINTERPRET_CAST`](../code-quality/c26490.md) — добавлен пример в C26490
- [`C26482 NO_DYNAMIC_ARRAY_INDEXING`](../code-quality/c26482.md) — добавлен пример в C26482
- [`C26471 NO_REINTERPRET_CAST_FROM_VOID_PTR`](../code-quality/c26471.md) — добавлен пример в C26471
- [`C26466 NO_STATIC_DOWNCAST_POLYMORPHIC`](../code-quality/c26466.md) — добавлен пример в C26466
- [`C26465 NO_CONST_CAST_UNNECESSARY`](../code-quality/c26465.md) — добавлен пример в C26465
- [`C26447 DONT_THROW_IN_NOEXCEPT`](../code-quality/c26447.md) — добавлен пример в C26447
- [`C26446 USE_GSL_AT`](../code-quality/c26446.md) — добавлен пример в C26446
- [`C26434 DONT_HIDE_METHODS`](../code-quality/c26434.md) — добавлен пример в C26434
- [`C26432 DEFINE_OR_DELETE_SPECIAL_OPS`](../code-quality/c26432.md) — добавлен пример в C26432
- [`C26402 DONT_HEAP_ALLOCATE_MOVABLE_RESULT`](../code-quality/c26402.md) — добавлен пример в C26402
- [`C26409 NO_NEW_DELETE`](../code-quality/c26409.md) — добавлен пример в C26409
- [`C26474 NO_IMPLICIT_CAST`](../code-quality/c26474.md) — обновлены сведения в C26474 с учетом уточненной информации о базовых и производных вариантах
## <a name="linux-with-microsoft-c-in-visual-studio"></a>Linux с Microsoft C++ в Visual Studio

### <a name="new-articles"></a>Новые статьи

- [Настройка проекта Linux CMake в Visual Studio](../linux/cmake-linux-configure.md)

### <a name="updated-articles"></a>Обновленные статьи

- [Создание проекта Linux на основе MSBuild C++ в Visual Studio](../linux/create-a-new-linux-project.md) — обновлены инструкции по созданию проекта Linux
- [Справка по ConnectionManager](../linux/connectionmanager-reference.md) — добавлены команды для изменения, очистки
- [Настройка проекта Linux CMake ы Visual Studio](../linux/cmake-linux-configure.md) — документация обновлена с учетом актуального пользовательского интерфейса
- [Развертывание, запуск и отладка проекта MSBuild Linux](../linux/deploy-run-and-debug-your-linux-project.md) — добавлено `GDB Path`

## <a name="cc-compiler-and-tools-errors-and-warnings"></a>Ошибки и предупреждения компилятора и средств C/C++

### <a name="new-articles"></a>Новые статьи

- [Предупреждение компилятора (уровень 4) C4388](../error-messages/compiler-warnings/c4388.md) — добавлено предупреждение C4388, обновлены предупреждения в версии 16.7

### <a name="updated-articles"></a>Обновленные статьи

- [Предупреждение компилятора (уровень 3) C4018](../error-messages/compiler-warnings/compiler-warning-level-3-c4018.md) — обновлены предупреждения 16.7
- [Предупреждение компилятора (уровень 4) C4389](../error-messages/compiler-warnings/compiler-warning-level-4-c4389.md) — обновлены предупреждения в версии 16.7
- [Предупреждения компилятора по версиям компилятора](../error-messages/compiler-warnings/compiler-warnings-by-compiler-version.md) — обновлены предупреждения в версии 16.7
- [Предупреждение компилятора с C4800 по C5999](../error-messages/compiler-warnings/compiler-warnings-c4800-through-c4999.md) — обновлены предупреждения в версии 16.7
- [Ошибка компилятора C3381](../error-messages/compiler-errors-2/compiler-error-c3381.md) — устранена ошибка cpp-docs 2493; обновлены комментарии и примеры

## <a name="cc-compiler-intrinsics-and-assembly-language"></a>Внутренние объекты компилятора и язык ассемблера

### <a name="updated-articles"></a>Обновленные статьи

- [Улучшения соответствия C++ в Visual Studio](../overview/cpp-conformance-improvements.md) — обновлено до заметок о выпуске 16.8
- [Справка и сообщество Microsoft C/C++](../overview/visual-cpp-help-and-community.md) — обновлены ссылки на сообщество разработчиков и на раздел вопросов и ответов в документации Майкрософт
- [C++ в Visual Studio](../overview/visual-cpp-in-visual-studio.md) — обновлены ссылки на сообщество разработчиков и на раздел вопросов и ответов в документации Майкрософт
- [Таблица соответствия Microsoft Visual C++ стандартам языка](../overview/visual-cpp-language-conformance.md) — обновлена таблица соответствия библиотеки C++ 20 стандартам языка, обновлена таблица функций языка для версии 16.7

## <a name="c-in-visual-studio"></a>C++ в Visual Studio

### <a name="updated-articles"></a>Обновленные статьи

- [`__restrict`](../cpp/extension-restrict.md)
- [Инструкция if-else (C++ )](../cpp/if-else-statement-cpp.md) — добавлено описание для грамматики `if/else`
- [`union`](../cpp/unions.md) — исправлен фрагмент кода

## <a name="cc-projects-and-build-systems"></a>Проекты и системы сборки C/C++

### <a name="new-articles"></a>Новые статьи

- [Файлы `.vcxproj` и подстановочные знаки](../build/reference/vcxproj-files-and-wildcards.md)
- [`/headerUnit` (использование IFC для единицы заголовка)](../build/reference/headerunit.md)
- [`/module:exportHeader` (создание единиц заголовков)](../build/reference/module-exportheader.md)
- [`/module:reference` (использование IFC для именованного модуля)](../build/reference/module-reference.md)
- [`/translateInclude` (преобразование директив include в директивы import)](../build/reference/translateinclude.md)
- [`/Zc:preprocessor` (включение режима соответствия препроцессора)](../build/reference/zc-preprocessor.md)

### <a name="updated-articles"></a>Обновленные статьи

- [`/permissive-` (соответствие требованиям стандартов)](../build/reference/permissive-standards-conformance.md) — обновлено до заметок о выпуске 16.8
- [`/clr` (компиляция среды CLR)](../build/reference/clr-common-language-runtime-compilation.md) — добавлено описание для `/clr`
- [pgosweep](../build/pgosweep.md) — добавлены дополнительные параметры pgosweep
- [Импорт данных с помощью `__declspec(dllimport)`](../build/importing-data-using-declspec-dllimport.md) — обновлен пример

## <a name="c-porting-and-upgrade-guide"></a>Руководство по переносу и обновлению C++

### <a name="updated-articles"></a>Обновленные статьи

- [Практическое руководство. Использование существующего кода C++ в приложении универсальной платформы Windows](../porting/how-to-use-existing-cpp-code-in-a-universal-windows-platform-app.md) — содержимое пересмотрено для упрощения понимания, а также обновлены примеры

## <a name="c-standard-library-stl-reference"></a>Справочник по стандартной библиотеке C++ (STL)

### <a name="new-articles"></a>Новые статьи

- [`<bit>`](../standard-library/bit.md)
- [Функции `<bit>`](../standard-library/bit-functions.md)
- [`endian` enum](../standard-library/bit-enum.md)

### <a name="updated-articles"></a>Обновленные статьи

- [`<ios>` typedefs](../standard-library/ios-typedefs.md) — обновлен пример для GitHub #2514
- [Класс `basic_string`](../standard-library/basic-string-class.md) — добавлено `_starts_with()`, `ends_with()`
- [`ios_base Class`](../standard-library/ios-base-class.md)
- [Класс `map`](../standard-library/map-class.md)
- [Класс `multimap`](../standard-library/multimap-class.md) — добавлено `contains()`
- [Класс `multiset`](../standard-library/multiset-class.md) — добавлено `contains()`
- [Класс `set`](../standard-library/set-class.md) — добавлено `contains()`
- [Класс `unordered_map`](../standard-library/unordered-map-class.md) — добавлено `contains()`
- [Класс `unordered_multimap`](../standard-library/unordered-multimap-class.md) — добавлено `contains()`
- [Класс `unordered_multiset`](../standard-library/unordered-multiset-class.md) — добавлено `contains()`
- [Класс `unordered_set`](../standard-library/unordered-set-class.md) — добавлено `contains()`
- [Класс `basic_string_view`](../standard-library/basic-string-view-class.md) — добавлено `starts_with()`, `ends_with()`
- [Функции `<bit>`](../standard-library/bit-functions.md) — обновлен синтаксис `nodiscard`

## <a name="community-contributors"></a>Участники сообщества

Указанные ниже пользователи в течение этого периода внесли свой вклад в улучшение документации по C++, C и Assembler. Спасибо! Дополнительные сведения о том, как внести свой вклад, см. в статье [Руководство для соавторов документации Майкрософт](/contribute/).

- [yecril71pl](https://github.com/yecril71pl) — Кристофер Йелейтон (Christopher Yeleighton) (4)
- [definedrisk](https://github.com/definedrisk) — Бен (Ben) (3)
- [BeardedFish](https://github.com/BeardedFish) — Дэриан Б (Darian B) (1)
- [codevenkat](https://github.com/codevenkat) (1)
- [eltociear](https://github.com/eltociear) — Икко Ашимине (Ikko Ashimine) (1)
- [fsb4000](https://github.com/fsb4000) — Игорь Жуков (Igor Zhukov) (1)
- [Jaiganeshkumaran](https://github.com/Jaiganeshkumaran) — Джиганеш Кумаран (Jaiganesh Kumaran) (1)
- [jogo-](https://github.com/jogo-) (1)
- [justanotheranonymoususer](https://github.com/justanotheranonymoususer) (1)
- [matrohin](https://github.com/matrohin) — Дмитрий Матрохин (Dmitry Matrokhin) (1)
- [mhemmit](https://github.com/mhemmit) (1)
- [MSDN-WhiteKnight](https://github.com/MSDN-WhiteKnight) — MSDN.WhiteKnight (1)
- [OdinTemple](https://github.com/OdinTemple) — Один Темпл (Odin Temple) (1)
- [r00tdr4g0n](https://github.com/r00tdr4g0n) — r00tdr4g0n (1)
- [sebkraemer](https://github.com/sebkraemer) — Себастиан Кремер (Sebastian Krämer) (1)
- [vtjnash](https://github.com/vtjnash) — Джеймсон Нэш (Jameson Nash) (1)
- [Youssef1313](https://github.com/Youssef1313) — Юссеф Виктор (Youssef Victor) (1)
- [zecozephyr](https://github.com/zecozephyr) — Джонатан Бэйли (Jonathan Bailey) (1)