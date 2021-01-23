---
title: Директивы pragma и pragma Ключевые слова __ и _Pragma
description: Описание pragma директив, доступных в Microsoft Visual C и C++ (компилятором MSVC)
ms.date: 01/19/2021
f1_keywords:
- '#pragma'
- _Pragma
- __pragma
helpviewer_keywords:
- '#pragma directives, C/C++'
- __pragma keyword
- _Pragma keyword
- pragma directives, C/C++
- pragmas, C/C++
- preprocessor
- pragmas
- preprocessor, pragmas
- pragma directives (#pragma)
no-loc:
- pragma
ms.openlocfilehash: fb6daf4c2912ea2168c38bfe2d1ae2650aaecc20
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713354"
---
# <a name="pragma-directives-and-the-__no-locpragma-and-_pragma-keywords"></a>Директивы pragma и `__pragma` `_Pragma` Ключевые слова и

Директивы директивы pragma определяют функции компилятора, зависящие от конкретного компьютера или операционной системы. **`__pragma`** Ключевое слово, относящееся только к компилятору Майкрософт, позволяет создавать pragma директивы кода внутри определений макросов. Стандартный **`_Pragma`** Оператор препроцессора появился в C99 и принят в c++ 11.

## <a name="syntax"></a>Синтаксис

> **`#pragma`***Строка токена*\
> **`__pragma(`***строка* **`)`** токена два подчеркивания в начале — конкретное расширение Майкрософт \
> **`_Pragma(`***строковый литерал* **`)`** C99

## <a name="remarks"></a>Примечания

Каждая реализация C и C++ поддерживает некоторые возможности, уникальные для хост-компьютера или операционной системы. Некоторые программы, например, должны выполнять точный контроль над расположением данных в памяти или управлять способом получения параметров определенными функциями. **`#pragma`** Директивы предлагают каждому компилятору возможность предоставлять функции для конкретного компьютера и операционной системы, сохраняя общую совместимость с языками C и C++.

Директивы директивы pragma зависят от конкретного компьютера или операционной системы и обычно отличаются для каждого компилятора. pragmaМожно использовать в условной директиве для предоставления новых функций препроцессора. Или используйте один из них, чтобы предоставить компилятору сведения, определяемые реализацией.

*Строка токена* — это последовательность символов, представляющая конкретную инструкцию компилятора и аргументы, если таковые имеются. Знак решетки ( **`#`** ) должен быть первым символом, не являющимся пробелом, в строке, содержащей pragma . Символы пробела могут разделять знак решетки и слово « pragma ». Далее **`#pragma`** напишите любой текст, который переводчик может проанализировать в виде токенов предварительной обработки. Аргумент для **`#pragma`** заключается в расширении макроса.

*Строка-литерал* — это входные данные `_Pragma` . Внешние кавычки и начальные и конечные пробелы удаляются. `\"` заменяется на `"` и `\\` заменяется на `\` .

Компилятор выдает предупреждение при обнаружении того pragma , что оно не распознается, и продолжит компиляцию.

Компиляторы Microsoft C и C++ распознают следующие pragma директивы:

:::row:::
   :::column span="":::
      [`alloc_text`](../preprocessor/alloc-text.md)\
      [`auto_inline`](../preprocessor/auto-inline.md)\
      [`bss_seg`](../preprocessor/bss-seg.md)\
      [`check_stack`](../preprocessor/check-stack.md)\
      [`code_seg`](../preprocessor/code-seg.md)\
      [`comment`](../preprocessor/comment-c-cpp.md)\
      [`component`](../preprocessor/component.md)\
      [`conform`](../preprocessor/conform.md)<sup>1</sup>\
      [`const_seg`](../preprocessor/const-seg.md)\
      [`data_seg`](../preprocessor/data-seg.md)\
      [`deprecated`](../preprocessor/deprecated-c-cpp.md)
   :::column-end:::
   :::column span="":::
      [`detect_mismatch`](../preprocessor/detect-mismatch.md)\
      [`endregion`](../preprocessor/region-endregion.md)\
      [`fenv_access`](../preprocessor/fenv-access.md)\
      [`float_control`](../preprocessor/float-control.md)\
      [`fp_contract`](../preprocessor/fp-contract.md)\
      [`function`](../preprocessor/function-c-cpp.md)\
      [`hdrstop`](../preprocessor/hdrstop.md)\
      [`include_alias`](../preprocessor/include-alias.md)\
      [`init_seg`](../preprocessor/init-seg.md)<sup>1</sup>\
      [`inline_depth`](../preprocessor/inline-depth.md)\
      [`inline_recursion`](../preprocessor/inline-recursion.md)
   :::column-end:::
   :::column span="":::
      [`intrinsic`](../preprocessor/intrinsic.md)\
      [`loop`](../preprocessor/loop.md)<sup>1</sup>\
      [`make_public`](../preprocessor/make-public.md)\
      [`managed`](../preprocessor/managed-unmanaged.md)\
      [`message`](../preprocessor/message.md)\
      [`omp`](../preprocessor/omp.md)\
      [`once`](../preprocessor/once.md)\
      [`optimize`](../preprocessor/optimize.md)\
      [`pack`](../preprocessor/pack.md)\
      [`pointers_to_members`](../preprocessor/pointers-to-members.md)<sup>1</sup>
   :::column-end:::
   :::column span="":::
      [`pop_macro`](../preprocessor/pop-macro.md)\
      [`push_macro`](../preprocessor/push-macro.md)\
      [`region`](../preprocessor/region-endregion.md)\
      [`runtime_checks`](../preprocessor/runtime-checks.md)\
      [`section`](../preprocessor/section.md)\
      [`setlocale`](../preprocessor/setlocale.md)\
      [`strict_gs_check`](../preprocessor/strict-gs-check.md)\
      [`unmanaged`](../preprocessor/managed-unmanaged.md)\
      [`vtordisp`](../preprocessor/vtordisp.md)<sup>1</sup>\
      [`warning`](../preprocessor/warning.md)
   :::column-end:::
:::row-end:::

<sup>1</sup> поддерживается только компилятором C++.

## <a name="pragma-directives-and-compiler-options"></a>Директивы pragma и параметры компилятора

Некоторые pragma директивы предоставляют те же функциональные возможности, что и параметры компилятора. Когда в pragma исходном коде достигается, он переопределяет поведение, заданное параметром компилятора. Например, если указано [`/Zp8`](../build/reference/zp-struct-member-alignment.md) , можно переопределить этот параметр компилятора для определенных разделов кода [`pack`](../preprocessor/pack.md) :

```cmd
cl /Zp8 some_file.cpp
```

```cpp
// some_file.cpp - packing is 8
// ...
#pragma pack(push, 1) - packing is now 1
// ...
#pragma pack(pop) - packing is 8 again
// ...
```

## <a name="the-__no-locpragma-keyword"></a>ключевое слово `__pragma()`;

Компилятор также поддерживает **`__pragma`** ключевое слово Microsoft, которое имеет те же функциональные возможности, что и **`#pragma`** директива. Разница заключается в том, что **`__pragma`** ключевое слово можно использовать в качестве встроенного в определении макроса. **`#pragma`** Директива не может использоваться в определении макроса, так как компилятор интерпретирует символ решетки (#) в директиве как [оператор строковый (#)](../preprocessor/stringizing-operator-hash.md).

В следующем примере кода показано, как **`__pragma`** ключевое слово может использоваться в макросе. Этот код взят из заголовка *мфкдуал. h* в образце ACDUAL в "примеры поддержки компилятора COM":

```cpp
#define CATCH_ALL_DUAL \
CATCH(COleException, e) \
{ \
_hr = e->m_sc; \
} \
AND_CATCH_ALL(e) \
{ \
__pragma(warning(push)) \
__pragma(warning(disable:6246)) /*disable _ctlState prefast warning*/ \
AFX_MANAGE_STATE(pThis->m_pModuleState); \
__pragma(warning(pop)) \
_hr = DualHandleException(_riidSource, e); \
} \
END_CATCH_ALL \
return _hr; \
```

## <a name="the-_pragma-preprocessing-operator-c99-c11"></a>`_Pragma`Оператор предварительной обработки (C99, c++ 11)

`_Pragma` Аналогично [`__pragma`](#the-__pragma-keyword) ключевому слову Microsoft, за исключением того, что оно является частью стандарта. Он появился для C в C99. Для C++ оно было представлено в C++ 11.

 Он позволяет размещать pragma директивы в определении макроса. Он содержит одну начальную подчеркивание `_` вместо двух начальных подчеркивания `__` , которое имеет ключевое слово Microsoft, а первая буква прописной.

Строковый литерал должен быть таким же, как в противном случае после *`#pragma`* оператора. Например:

```c
#pragma message("the #pragma way")
_Pragma ("message( \"the _Pragma way\")") 
```

Кавычки и обратные косые черты должны быть экранированы, как показано выше. pragmaСтрока, которая не распознана, игнорируется.

В следующем примере кода показано, как **`_Pragma`** ключевое слово можно использовать в макросе, похожем на утверждение, если не нужно получать предупреждение, если условие выражения имеет значение Constant. 

В определении макроса используется `do` - `while(0)` идиома для макросов с несколькими операторами, чтобы его можно было использовать, как будто это одна инструкция. Дополнительные сведения см. в разделе [Многострочный макрос на языке C](https://stackoverflow.com/questions/1067226/c-multi-line-macro-do-while0-vs-scope-block) Stack Overflow. **`_Pragma`** Оператор применяется только к строке кода, следующей за ней.

```C
// Compile with /W4

#include <stdio.h>
#include <stdlib.h>

#define MY_ASSERT(BOOL_EXPRESSION) \
    do { \
        _Pragma("warning(suppress: 4127)") /* C4127 conditional expression is constant */  \
        if (!(BOOL_EXPRESSION)) {   \
            printf("MY_ASSERT FAILED: \"" #BOOL_EXPRESSION "\" on %s(%d)", __FILE__, __LINE__); \
            exit(-1); \
        } \
    } while (0)

int main()
{
    MY_ASSERT(0 && "Note that there is no warning: C4127 conditional expression is constant");

    return 0;
}
```

## <a name="see-also"></a>См. также раздел

[Справочник по препроцессору в C/C++](../preprocessor/c-cpp-preprocessor-reference.md)\
[pragmaДирективы C](../c-language/c-pragmas.md)\
[Ключевые слова](../cpp/keywords-cpp.md)
