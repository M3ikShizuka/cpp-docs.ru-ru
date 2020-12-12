---
description: 'Дополнительные сведения: __unaligned'
title: __unaligned
ms.date: 12/17/2018
f1_keywords:
- __unaligned_cpp
- __unaligned
- _unaligned
helpviewer_keywords:
- __unaligned keyword [C++]
ms.assetid: 0cd83aad-1840-47e3-ad33-59bfcbe6375b
ms.openlocfilehash: f5afd0c6c1a506cbaeb03d497e64eac743ecc4df
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97145760"
---
# <a name="__unaligned"></a>__unaligned

**Зависит от корпорации Майкрософт**. При объявлении указателя с **`__unaligned`** модификатором компилятор предполагает, что указатель обращается к несогласованным данным. Следовательно, код, соответствующий платформе, создается для управления несогласованными операциями чтения и записи через указатель.

## <a name="remarks"></a>Комментарии

Этот модификатор описывает выравнивание данных, адресованных указателю; Предполагается, что указатель должен быть согласован.

Необходимость в **`__unaligned`** ключевом слове зависит от платформы и среды. Неправильное пометка данных может привести к проблемам, от снижения производительности до сбоев оборудования. **`__unaligned`** Модификатор недопустим для платформы x86.

Для совместимости с предыдущими версиями аргумент **`_unaligned`** является синонимом, **`__unaligned`** если только параметр компилятора не [ `/Za` \( отключает расширения языка)](../build/reference/za-ze-disable-language-extensions.md) .

Дополнительные сведения о выравнивании см. в разделах:

- [`align`](../cpp/align-cpp.md)

- [`alignof` Станции](../cpp/alignof-operator.md)

- [`pack`](../preprocessor/pack.md)

- [`/Zp` (Выравнивание членов структуры)](../build/reference/zp-struct-member-alignment.md)

- [Примеры выравнивания структуры](../build/x64-software-conventions.md#examples-of-structure-alignment)

## <a name="see-also"></a>См. также раздел

[Ключевые слова](../cpp/keywords-cpp.md)
