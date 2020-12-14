---
description: 'Дополнительные сведения: __movsb'
title: __movsb
ms.date: 09/02/2019
f1_keywords:
- __movsb
helpviewer_keywords:
- movsb instruction
- rep movsb instruction
- __movsb intrinsic
ms.assetid: ba5469f6-f797-4cd2-bee8-74c7666c26d4
ms.openlocfilehash: 6e4a9ba7482f7f614b80bd0596111874f0087c86
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97222454"
---
# <a name="__movsb"></a>__movsb

**Блок, относящийся только к системам Microsoft**

Создает инструкцию перемещения строки ( `rep movsb` ).

## <a name="syntax"></a>Синтаксис

```C
void __movsb(
   unsigned char* Destination,
   unsigned const char* Source,
   size_t Count
);
```

### <a name="parameters"></a>Параметры

*Местоназначение*\
заполняет Указатель на место назначения копии.

*Источника*\
окне Указатель на источник копии.

*Расчета*\
окне Число байтов для копирования.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__movsb`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

В результате первые `Count` байты, на которые указывает, `Source` копируются в `Destination` строку.

Эта процедура доступна только как встроенная функция.

## <a name="example"></a>Пример

```cpp
// movsb.cpp
// processor: x86, x64
#include <stdio.h>
#include <intrin.h>

#pragma intrinsic(__movsb)

int main()
{
    unsigned char s1[100];
    unsigned char s2[100] = "A big black dog.";
    __movsb(s1, s2, 100);

    printf_s("%s %s", s1, s2);
}
```

```Output
A big black dog. A big black dog.
```

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
