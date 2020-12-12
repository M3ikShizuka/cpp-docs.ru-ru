---
description: 'Дополнительные сведения: использование операторов в блоках __asm'
title: Использование операторов в блоках __asm
ms.date: 08/30/2018
helpviewer_keywords:
- brackets [ ]
- brackets [ ], __asm blocks
- __asm keyword [C++], operators
- square brackets [ ], __asm blocks
- operators [C++], using in __asm blocks
- square brackets [ ]
ms.assetid: a26ccfd4-40ae-4a61-952f-c417982aa8dd
ms.openlocfilehash: 266d840e6cb407d45c1d3a49bed6a2390e52aa2e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97121853"
---
# <a name="using-operators-in-__asm-blocks"></a>Использование операторов в блоках __asm

**Блок, относящийся только к системам Microsoft**

**`__asm`** Блок не может использовать специальные операторы C или C++, например **<<** оператор. Однако операторы, совместно используемые C и MASM, такие как оператор, считаются операторами \* языка ассемблера. Например, за пределами **`__asm`** блока квадратные скобки (**[]**) обрабатываются как вложенные индексы массива, которые в языке C автоматически масштабируются до размера элемента в массиве. Внутри **`__asm`** блока они отображаются в виде оператора MASM index, который возвращает немасштабированное смещение в байтах от любого объекта данных или метки (не только для массива). В следующем примере кода демонстрируется различие.

```cpp
int array[10];

__asm mov array[6], bx ;  Store BX at array+6 (not scaled)

array[6] = 0;         /* Store 0 at array+24 (scaled) */
```

Первая ссылка на `array` не масштабируется, вторая — масштабируется. Обратите внимание, что оператор **Type** можно использовать для достижения масштабирования на основе константы. Например, следующие инструкции эквивалентны.

```cpp
__asm mov array[6 * TYPE int], 0 ; Store 0 at array + 24

array[6] = 0;                   /* Store 0 at array + 24 */
```

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Использование C или C++ в блоках __asm](../../assembler/inline/using-c-or-cpp-in-asm-blocks.md)<br/>
