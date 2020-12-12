---
description: 'Дополнительные сведения о: discard_block_engine классе'
title: Класс discard_block_engine
ms.date: 11/04/2016
f1_keywords:
- random/std::discard_block_engine
helpviewer_keywords:
- discard_block_engine class
ms.assetid: aa84808e-38fe-4fa0-9f73-d5b9a653345b
ms.openlocfilehash: 0879dacac70afc78a9c77314ce5042580c6cbb39
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324520"
---
# <a name="discard_block_engine-class"></a>Класс discard_block_engine

Создает случайную последовательность, удаляя значения, возвращенные базовым механизмом.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Engine, size_t P, size_t R>
class discard_block_engine;
```

### <a name="parameters"></a>Параметры

*Ядре*\
Тип базового механизма.

*Ш*\
**Размер блока**. Количество значений в каждом блоке.

*Cерверный*\
**Используемый блок**. Количество используемых значений в каждом блоке. Остальные отбрасываются ( `P`  -  `R` ). **Предварительное условие**: `0 < R ≤ P`

## <a name="members"></a>Элементы

`discard_block_engine::discard_block_engine`\
`discard_block_engine::base`\
`discard_block_engine::base_type`\
`discard_block_engine::discard`\
`discard_block_engine::operator()`\
`discard_block_engine::seed`

Дополнительные сведения о членах подсистемы см [\<random>](../standard-library/random.md) . в разделе.

## <a name="remarks"></a>Комментарии

Этот шаблон класса описывает адаптер подсистемы, создающий значения путем удаления некоторых значений, возвращенных базовым механизмом.

## <a name="requirements"></a>Требования

**Заголовок:**\<random>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[\<random>](../standard-library/random.md)
