---
description: 'Дополнительные сведения: `__declspec`'
title: __declspec
ms.date: 03/21/2019
f1_keywords:
- __declspec_cpp
- __declspec
- _declspec
helpviewer_keywords:
- __declspec keyword [C++]
ms.openlocfilehash: 1a8644bc05319332967ffd7934e6799408c3d36d
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102465532"
---
# `__declspec`

**Блок, относящийся только к системам Microsoft**

В синтаксисе расширенных атрибутов для указания сведений о классе хранения используется **`__declspec`** ключевое слово, которое указывает, что экземпляр заданного типа должен храниться в указанном ниже атрибуте класса хранения, связанном с Майкрософт. Примеры других модификаторов класса хранения включают **`static`** **`extern`** Ключевые слова и. Однако эти ключевые слова — часть спецификации ANSI языков C и C++, и как таковые они не описаны расширенным синтаксисом атрибутов. Расширенный синтаксис атрибутов упрощает и стандартизирует расширения для систем Microsoft в соответствии с правилами языков C и С++.

## <a name="grammar"></a>Грамматика

*`decl-specifier`*:\
&emsp;**`__declspec (`**  *`extended-decl-modifier-seq`*  **`)`**

*`extended-decl-modifier-seq`*:\
&emsp; *`extended-decl-modifier`* <sub>необ.</sub> \
&emsp;*`extended-decl-modifier`* *`extended-decl-modifier-seq`*

*`extended-decl-modifier`*:\
&emsp;**`align(`***число***`)`**\
&emsp;**`allocate("`***сегнаме***`")`**\
&emsp;**`allocator`**\
&emsp;**`appdomain`**\
&emsp;**`code_seg("`***сегнаме***`")`**\
&emsp;**`deprecated`**\
&emsp;**`dllimport`**\
&emsp;**`dllexport`**\
&emsp;**`jitintrinsic`**\
&emsp;**`naked`**\
&emsp;**`noalias`**\
&emsp;**`noinline`**\
&emsp;**`noreturn`**\
&emsp;**`nothrow`**\
&emsp;**`novtable`**\
&emsp;**`no_sanitize_address`**\
&emsp;**`process`**\
&emsp;**`property(`**{ **`get=`** _Get-Func-Name_ &#124; **`,put=`** _Вставить-Func-Name_ }**`)`**\
&emsp;**`restrict`**\
&emsp;**`safebuffers`**\
&emsp;**`selectany`**\
&emsp;**`spectre(nomitigation)`**\
&emsp;**`thread`**\
&emsp;**`uuid("`***Комобжектгуид***`")`**

Пробел отделяет последовательность модификаторов объявления. Примеры приведены в дальнейших разделах.

Грамматика расширенных атрибутов поддерживает следующие атрибуты классов хранения, предназначенные для Майкрософт:,,,,,,,,,,,,,,,,,,,, [`align`](../cpp/align-cpp.md) [`allocate`](../cpp/allocate.md) [`allocator`](../cpp/allocator.md) [`appdomain`](../cpp/appdomain.md) [`code_seg`](../cpp/code-seg-declspec.md) [`deprecated`](../cpp/deprecated-cpp.md) [`dllexport`](../cpp/dllexport-dllimport.md) [`dllimport`](../cpp/dllexport-dllimport.md) [`jitintrinsic`](../cpp/jitintrinsic.md) [`naked`](../cpp/naked-cpp.md) [`noalias`](../cpp/noalias.md) [`noinline`](../cpp/noinline.md) [`noreturn`](../cpp/noreturn.md) [`nothrow`](../cpp/nothrow-cpp.md) [`novtable`](../cpp/novtable.md) [`no_sanitize_address`](../cpp/no-sanitize-address.md) [`process`](../cpp/process.md) [`restrict`](../cpp/restrict.md) [`safebuffers`](../cpp/safebuffers.md) [`selectany`](../cpp/selectany.md) [`spectre`](../cpp/spectre.md) и [`thread`](../cpp/thread.md) . Он также поддерживает следующие атрибуты COM-Object: [`property`](../cpp/property-cpp.md) и [`uuid`](../cpp/uuid-cpp.md) .

**`code_seg`** **`dllexport`** **`dllimport`** Атрибуты класса хранения,,,,, **`naked`** **`noalias`** **`nothrow`** , **`no_sanitize_address`** , **`property`** , **`restrict`** , **`selectany`** , **`thread`** и **`uuid`** являются свойствами только объявления объекта или функции, к которым они применяются. **`thread`** Атрибут влияет только на данные и объекты. **`naked`** Атрибуты и **`spectre`** влияют только на функции. **`dllimport`** Атрибуты и **`dllexport`** влияют на функции, данные и объекты. **`property`** Атрибуты, **`selectany`** и **`uuid`** влияют на COM-объекты.

Для совместимости с предыдущими версиями аргумент **`_declspec`** является синонимом, **`__declspec`** если только параметр компилятора [/Za не \( отключил расширения языка)](../build/reference/za-ze-disable-language-extensions.md) .

**`__declspec`** Ключевые слова должны располагаться в начале простого объявления. Компилятор игнорирует, без предупреждения, все **`__declspec`** Ключевые слова, помещенные после * или &, а также перед идентификатором переменной в объявлении.

**`__declspec`** Атрибут, указанный в начале объявления определяемого пользователем типа, применяется к переменной этого типа. Пример:

```cpp
__declspec(dllimport) class X {} varX;
```

В этом случае атрибут применяется к `varX`. **`__declspec`** Атрибут, помещенный после **`class`** **`struct`** ключевого слова или, применяется к определяемому пользователем типу. Пример:

```cpp
class __declspec(dllimport) X {};
```

В этом случае атрибут применяется к `X`.

Ниже приведены общие рекомендации по использованию **`__declspec`** атрибута для простых объявлений.

*описателе-описатель-seq* *init-декларатор-List*;

*Описатель decl-seq* должен содержать, помимо прочего, базовый тип (например,, **`int`** **`float`** **`typedef`** или имя класса), класс хранения (например **`static`** , **`extern`** ) или **`__declspec`** расширение. Элемент *init-декларатор-List* должен содержать, помимо прочего, указательную часть объявлений. Пример:

```cpp
__declspec(selectany) int * pi1 = 0;   //Recommended, selectany & int both part of decl-specifier
int __declspec(selectany) * pi2 = 0;   //OK, selectany & int both part of decl-specifier
int * __declspec(selectany) pi3 = 0;   //ERROR, selectany is not part of a declarator
```

В следующем примере кода объявлена целочисленная локальная переменная потока и инициализирована с использованием следующего значения:

```cpp
// Example of the __declspec keyword
__declspec( thread ) int tls_i = 1;
```

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Словами](../cpp/keywords-cpp.md)\
[Расширенные атрибуты классов хранения в C](../c-language/c-extended-storage-class-attributes.md)
