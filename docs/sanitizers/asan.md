---
title: аддресссанитизер
description: Описание верхнего уровня функции Аддресссанитизер для Microsoft C/C++.
ms.date: 03/05/2021
f1_keywords:
- AddressSanitizer
helpviewer_keywords:
- ASan
- AddressSanitizer
- Address Sanitizer
- compiling for AddressSanitizer
ms.openlocfilehash: db1760a37c610493cd3a3d95ab5e77b29bf89400
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471279"
---
# <a name="addresssanitizer"></a>аддресссанитизер

## <a name="overview"></a>Обзор

Языки C & C++ являются мощными, но могут пострадать от класса ошибок, влияющих на правильность программы и безопасность программ. Начиная с Visual Studio 2019 версии 16,9, компилятор Microsoft C/C++ (КОМПИЛЯТОРОМ MSVC) и интегрированная среда разработки поддерживают *аддресссанитизер*. Аддресссанитизер (Асан) — это технология компилятора и среды выполнения, которая предоставляет множество трудно обнаруживаемых ошибок с **нулевым** числом ложных срабатываний:

- Несоответствия между разблокировками и [развыделениями](error-alloc-dealloc-mismatch.md) и [ `new` / `delete` несоответствия типов](error-new-delete-type-mismatch.md)
- [Слишком большие выделения памяти для кучи](error-allocation-size-too-big.md)
- [ `calloc` переполнение](error-calloc-overflow.md) и [ `alloca` переполнение](error-dynamic-stack-buffer-overflow.md)
- [Двойная бесплатная](error-double-free.md) и [используемая после бесплатной установки](error-heap-use-after-free.md)
- [Переполнение глобальной переменной](error-global-buffer-overflow.md)
- [Heap buffer overflow;](error-heap-buffer-overflow.md)
- [Недопустимое выравнивание выровненных значений](error-invalid-allocation-alignment.md)
- [`memcpy`](error-memcpy-param-overlap.md)и [ `strncat` Перекрытие параметров](error-strncat-param-overlap.md)
- [Переполнение буфера стека](error-stack-buffer-overflow.md) и [потеря значимости](error-stack-buffer-underflow.md)
- [Использование стека `return` после](error-stack-use-after-return.md) и [использовать после Scope](error-stack-use-after-scope.md)
- [Использование памяти после ее переделки](error-use-after-poison.md)

Используйте Аддресссанитизер, чтобы сократить время, потраченное на:

- Базовая правильность
- Переносимость между платформами
- Безопасность
- нагрузочное тестирование
- Интеграция нового кода

Аддресссанитизер, изначально [введенные Google](https://www.usenix.org/conference/atc12/technical-sessions/presentation/serebryany), — это мощная альтернатива обеим [ `/RTC` (проверкам ошибок времени выполнения)](../build/reference/rtc-run-time-error-checks.md) и [ `/analyze` (статический анализ)](../build/reference/analyze-code-analysis.md). Она предоставляет технологии поиска ошибок во время выполнения, которые используют существующие системы сборки и существующие ресурсы тестирования напрямую.

Аддресссанитизер интегрирована с системой проектов Visual Studio, системой сборки CMak и интегрированной средой разработки. Проекты могут включать Аддресссанитизер, устанавливая свойство проекта или используя один дополнительный параметр компилятора: **`/fsanitize=address`** . Новый параметр совместим со всеми уровнями оптимизации и конфигураций для x86 и x64. Однако она несовместима с [Edit-and-Continue](/visualstudio/debugger/edit-and-continue-visual-cpp), [инкрементной компоновкой](../build/reference/incremental-link-incrementally.md)и [`/RTC`](../build/reference/rtc-run-time-error-checks.md) .

Начиная с Visual Studio 2019 версии 16,9, технология Аддресссанитизер Майкрософт обеспечивает интеграцию с интегрированной средой разработки Visual Studio. При необходимости можно создать файл аварийного дампа при обнаружении ошибки в среде выполнения. Если задать `ASAN_SAVE_DUMPS=MyFileName.dmp` переменную среды перед запуском программы, то файл аварийного дампа будет создан с дополнительными метаданными для эффективной отладки с точной [неустранимой](#crash-dumps) диагностикой ошибок. Эти файлы дампа упрощают расширенное использование Аддресссанитизер для:

- Тестирование локального компьютера,
- Локальное распределенное тестирование и
- Облачные рабочие процессы для тестирования.

### <a name="install-the-addresssanitizer"></a>Установка Аддресссанитизер

Интеграция и библиотеки интегрированной среды разработки Аддресссанитизер устанавливаются по умолчанию с рабочими нагрузками C++ в Visual Studio Installer. Однако при обновлении с более ранней версии Visual Studio 2019 используйте установщик, чтобы включить поддержку Асан после обновления:

:::image type="content" source="media/asan-installer-option.png" alt-text="Visual Studio Installer снимок экрана с выделением компонента C++ Аддресссанитизер":::

Вы можете выбрать команду **изменить** в существующей установке Visual Studio из Visual Studio Installer, чтобы перейти к показанному выше экрану.

> [!NOTE]
> Если вы запустите Visual Studio на новом обновлении, но не установили Асан, вы получите сообщение об ошибке при выполнении кода:
>
> LNK1356: не удается найти библиотеку "clang_rt. asan_dynamic-i386. lib"

### <a name="use-the-addresssanitizer"></a><a name="using-asan"></a> Использование Аддресссанитизер

Приступите к созданию исполняемых файлов с **`/fsanitize=address`** помощью параметра компилятора, используя любой из следующих распространенных методов разработки:

- Сборки из командной строки
- Система проектов Visual Studio
- Интеграция с Visual Studio CMak

 Выполните повторную компиляцию, а затем запустите программу обычным образом. Эта генерация кода предоставляет [множество типов точного обнаружения ошибок](#error-types). Эти ошибки выводятся тремя способами: в интегрированной среде разработки отладчика, в командной строке или в [новом типе файла дампа](#crash-dumps) для точной обработки вне строки.

Корпорация Майкрософт рекомендует использовать Аддресссанитизер в этих трех стандартных рабочих процессах:

- **Внутренний цикл разработчика**
  - Visual Studio — [Командная строка](#command-prompt)
  - Visual Studio — [система проектов](#ide-msbuild)
  - Visual Studio — [CMAK](#ide-cmake)

- Непрерывная **интеграция и** непрерывная разработка интеграции
  - Отчеты об ошибках — [новые файлы дампа аддресссанитизер](#crash-dumps)

- **Нечеткое** создание с помощью оболочки [либфуззер](https://llvm.org/docs/LibFuzzer.html)
  - [Azure Онефузз](https://www.microsoft.com/security/blog/2020/09/15/microsoft-onefuzz-framework-open-source-developer-tool-fix-bugs/)
  - Локальный компьютер

В этой статье рассматриваются сведения, необходимые для включения трех рабочих процессов, перечисленных выше. Эти сведения относятся к **зависящей от платформы** реализации Windows 10 аддресссанитизер. Эта документация дополняет отличную документацию от [Google, Apple и GCC](#external-docs) уже опубликованных.

> [!NOTE]
> Текущая поддержка ограничена x86 и x64 в Windows 10. [Отправьте нам отзыв](https://aka.ms/vsfeedback/browsecpp) о том, что вы хотели бы увидеть в будущих выпусках. Ваши отзывы помогают нам определить приоритеты для других таких систем, как,,, **`/fsanitize=thread`** **`/fsanitize=leak`** **`/fsanitize=memory`** **`/fsanitize=undefined`** или **`/fsanitize=hwaddress`** . Вы можете [сообщить об ошибках здесь](https://aka.ms/feedback/report?space=62) , если возникают проблемы.

## <a name="use-the-addresssanitizer-from-a-developer-command-prompt"></a><a name="command-prompt"></a> Использование Аддресссанитизер из командной строки разработчика

Используйте **`/fsanitize=address`** параметр компилятора в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts) , чтобы включить компиляцию для среды выполнения аддресссанитизер. **`/fsanitize=address`** Параметр совместим со всеми существующими уровнями оптимизации C++ или C (например,,,, `/Od` `/O1` `/O2` `/O2 /GL` и `PGO` ). Параметр работает со статическими и динамическими библиотек CRT (например,, `/MD` , `/MDd` `/MT` и `/MTd` ). Он работает независимо от того, создаете ли вы файл EXE или DLL. Отладочная информация необходима для оптимального форматирования стеков вызовов. В приведенном ниже примере `cl /fsanitize=address /Zi` передается в командной строке.

Библиотеки Аддресссанитизер (LIB-файлы) автоматически связываются. Дополнительные сведения см. в статье [Справочник по языку аддресссанитизер, сборке и отладке](asan-building.md).

### <a name="example---basic-global-buffer-overflow"></a>Пример базового глобального буфера переполнения

```cpp
// basic-global-overflow.cpp
#include <stdio.h>
int x[100];
int main() {
    printf("Hello!\n");
    x[100] = 5; // Boom!
    return 0;
}
```

Использование командной строки разработчика для Visual Studio 2019, компиляция *`main.cpp`* с помощью `/fsanitize=address /Zi`

:::image type="content" source="media/asan-command-basic-global-overflow.png" alt-text="Снимок экрана командной строки с командой для компиляции с параметрами Аддресссанитизер.":::

При запуске в результате выполнения в *`main.exe`* командной строке создается отформатированный отчет об ошибках, показанный ниже.

Рассмотрите «наложенные» красные квадратики, которые выделяют семь ключевых фрагментов информации:

:::image type="content" source="media/asan-basic-global-overflow.png" alt-text="Снимок экрана отладчика, иллюстрирующий базовую ошибку глобального переполнения.":::

### <a name="red-highlights-from-top-to-bottom"></a>Красные выделения, сверху вниз

1. Ошибка безопасности памяти — это переполнение глобального буфера.
2. Существует **4 байта** (32 бит), которые **хранятся** за пределами определяемой пользователем переменной.
3. Хранилище заняло функцию, `main()` определенную в файле в `basic-global-overflow.cpp` строке 7.
4. Переменная с именем `x` определяется в Басик-Глобал-оверфлов. cpp в строке 3, начиная со столбца 8.
5. Эта глобальная переменная `x` имеет размер 400 байт
6. Точный [теневой байт](./asan-shadow-bytes.md) , описывающий адрес, являющийся целевым для хранилища, имеет значение `0xf9`
7. В условных обозначениях теневых байтов написано `0xf9` область заполнения справа от `int x[100]`

> [!NOTE]
> Имена функций в стеке вызовов создаются через [Симболизер LLVM](https://llvm.org/docs/CommandGuide/llvm-symbolizer.html) , который вызывается средой выполнения при возникновении ошибки.

## <a name="use-the-addresssanitizer-in-visual-studio"></a><a name="ide-msbuild"></a> Использование Аддресссанитизер в Visual Studio

Аддресссанитизер интегрирован с интегрированной средой разработки Visual Studio. Чтобы включить Аддресссанитизер для проекта MSBuild, щелкните правой кнопкой мыши проект в обозреватель решений и выберите пункт **Свойства**. В диалоговом окне **страницы свойств** выберите **Свойства конфигурации**  >  **C/C++**  >  **Общие**, а затем измените свойство **включить аддресссанитизер** . Выберите **ОК** для сохранения внесенных изменений.

:::image type="content" source="media/asan-project-system-dialog.png" alt-text="Снимок экрана: диалоговое окно страниц свойств с отображением свойства &quot;включить Аддресссанитизер&quot;.":::

Чтобы выполнить сборку из интегрированной среды разработки, отказаться от всех [несовместимых параметров](./asan-known-issues.md#incompatible-options). Для существующего проекта, скомпилированного с помощью **`/Od`** (или режима отладки), может потребоваться отключить следующие параметры:

- Отключить режим ["изменить и продолжить"](/visualstudio/debugger/how-to-enable-and-disable-edit-and-continue)
- Выключить [ `/RTC1` (проверки среды выполнения)](../build/reference/rtc-run-time-error-checks.md)
- Выключить [ `/INCREMENTAL` (инкрементное связывание)](../build/reference/incremental-link-incrementally.md)

Чтобы создать и запустить отладчик, введите **F5**. Это окно появится в Visual Studio:

:::image type="content" source="media/asan-global-buffer-overflow-F5.png" alt-text="Снимок экрана отладчика, отображающий ошибку переполнения глобального буфера.":::

## <a name="using-the-addresssanitizer-from-visual-studio-cmake"></a><a name="ide-cmake"></a> Использование Аддресссанитизер из Visual Studio: CMak

Чтобы включить Аддресссанитизер для [проекта CMAK, созданного для целевой платформы Windows](../build/cmake-projects-in-visual-studio.md), сделайте следующее:

1. Откройте раскрывающийся список **конфигурации** на панели инструментов в верхней части интегрированной среды разработки и выберите **Управление конфигурациями**.

   :::image type="content" source="media/asan-cmake-configuration-dropdown.png" alt-text="Снимок экрана: раскрывающийся список конфигурации CMak.":::

   При выборе этого варианта открывается редактор параметров проекта CMak, который сохраняется в CMakeSettings.jsв файле.

1. Выберите ссылку **изменить JSON** в редакторе. Этот выбор переключает представление на необработанный JSON.

1. Добавьте свойство: **"аддресссанитизеренаблед": true**

   Это изображение CMakeSettings.jsпосле этого изменения:

   :::image type="content" source="media/asan-cmake-json.png" alt-text="Снимок экрана: представление текстового редактора CMakeSettings.json.":::

1. Нажмите **клавиши CTRL + S** , чтобы сохранить этот JSON файл, а затем введите **F5** для перекомпиляции и запуска в отладчике.

На этом снимке экрана показана ошибка сборки CMak.

:::image type="content" source="media/asan-cmake-error-f5.png" alt-text="Снимок экрана сообщения об ошибке сборки CMak.":::

## <a name="addresssanitizer-crash-dumps"></a><a name="crash-dumps"></a> Аддресссанитизер аварийные дампы

Мы предоставили новые функции в Аддресссанитизер для использования с облачными и распределенными рабочими процессами. Эта функция позволяет автономно просматривать ошибку Аддресссанитизер в интегрированной среде разработки. Эта ошибка накладывается поверх источника, как и при работе в динамическом сеансе отладки.

Эти новые файлы дампа могут привести к эффективному анализу ошибки. Вам не нужно повторно выполнять или искать удаленные данные или найти компьютер, который вышел из системы.

Чтобы создать новый тип файла дампа, который можно просмотреть в Visual Studio на другом компьютере позднее, выполните следующие действия.

```cmd
set ASAN_SAVE_DUMPS=MyFileName.dmp
```

Начиная с Visual Studio 16,9 можно отобразить **точную диагностику ошибки, которая** хранится в *`*.dmp`* файле, поверх исходного кода.

[Эта новая функция аварийного дампа](./asan-offline-crash-dumps.md) позволяет выполнять облачные рабочие процессы или распределенное тестирование. Его также можно использовать для получения подробной, практичной ошибки в любом сценарии.

## <a name="example-errors"></a><a name="error-types"></a> Примеры ошибок

Аддресссанитизер может обнаружить несколько типов ошибок неправильного использования памяти. Ниже приведено множество ошибок времени выполнения, о которых сообщается при запуске двоичных файлов, скомпилированных с помощью **`/fsanitize=address`** параметра компилятора аддресссанитизер ():

- [`alloc-dealloc-mismatch`](error-alloc-dealloc-mismatch.md)
- [`allocation-size-too-big`](error-allocation-size-too-big.md)
- [`calloc-overflow`](error-calloc-overflow.md)
- [`double-free`](error-double-free.md)
- [`dynamic-stack-buffer-overflow`](error-dynamic-stack-buffer-overflow.md)
- [`global-buffer-overflow`](error-global-buffer-overflow.md)
- [`heap-buffer-overflow`](error-heap-buffer-overflow.md)
- [`heap-use-after-free`](error-heap-use-after-free.md)
- [`invalid-allocation-alignment`](error-invalid-allocation-alignment.md)
- [`memcpy-param-overlap`](error-memcpy-param-overlap.md)
- [`new-delete-type-mismatch`](error-new-delete-type-mismatch.md)
- [`stack-buffer-overflow`](error-stack-buffer-overflow.md)
- [`stack-buffer-underflow`](error-stack-buffer-underflow.md)
- [`stack-use-after-return`](error-stack-use-after-return.md)
- [`stack-use-after-scope`](error-stack-use-after-scope.md)
- [`strncat-param-overlap`](error-strncat-param-overlap.md)
- [`use-after-poison`](error-use-after-poison.md)

Дополнительные сведения об этих примерах см. в разделе [аддресссанитизер Error examples](./asan-error-examples.md).

## <a name="differences-with-clang-120"></a><a name="differences"></a> Отличия от Clang 12,0

В настоящее время КОМПИЛЯТОРОМ MSVC отличается от Clang 12,0 в двух функциональных областях:

- **Stack-use-после-Scope** — этот параметр включен по умолчанию и не может быть отключен.
- **Stack-после-return** — эта функция требует дополнительного параметра компилятора и недоступна для установки только `ASAN_OPTIONS` .

Эти решения были сделаны, чтобы сократить матрицу тестирования, необходимую для реализации этой первой версии.

В Visual Studio 2019 16,9 не включались функции, которые могут привести к ложным срабатываниям. Эта дисциплина обеспечивает эффективную целостность тестирования, необходимую при рассмотрении взаимодействия с десятилетиями существующего кода. В более поздних выпусках можно рассмотреть дополнительные возможности:

- [Руткитом порядка инициализации](https://github.com/google/sanitizers/wiki/AddressSanitizerInitializationOrderFiasco)
- [Переполнение внутри объекта](https://github.com/google/sanitizers/wiki/AddressSanitizerIntraObjectOverflow)
- [Переполнение контейнера](https://github.com/google/sanitizers/wiki/AddressSanitizerContainerOverflow)
- [Вычитание указателей/сравнение](https://gcc.gnu.org/onlinedocs/gcc/Instrumentation-Options.html)

Дополнительные сведения см. [в статье сборка для аддресссанитизер с помощью компилятором MSVC](./asan-building.md).

## <a name="existing-industry-documentation"></a><a name="external-docs"></a> Существующая отраслевая документация

Для этих языков и реализаций технологии Аддресссанитизер уже существует обширная документация.

- [Google](https://github.com/google/sanitizers/wiki/AddressSanitizer)
- [Apple](https://developer.apple.com/documentation/xcode/diagnosing_memory_thread_and_crash_issues_early);
- [GCC](https://gcc.gnu.org/onlinedocs/gcc/Instrumentation-Options.html)

В этой основополагающуюной статье о [аддресссанитизер](https://www.usenix.org/system/files/conference/atc12/atc12-final39.pdf) описывается реализация.

## <a name="see-also"></a>См. также раздел

[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
