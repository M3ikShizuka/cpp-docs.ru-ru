---
description: Дополнительные сведения об pragma директиве strict_gs_check в Microsoft C/C++
title: strict_gs_check pragma
ms.date: 01/22/2021
f1_keywords:
- strict_gs_check
- strict_gs_check_CPP
helpviewer_keywords:
- strict_gs_check pragma
- pragma, strict_gs_check
no-loc:
- pragma
ms.openlocfilehash: 4a224c42dc30227e5bd9a7142c807f7cebc34614
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713159"
---
# <a name="strict_gs_check-no-locpragma"></a>`strict_gs_check` pragma

Это pragma обеспечивает улучшенную проверку безопасности.

## <a name="syntax"></a>Синтаксис

> **`#pragma strict_gs_check(`** [ **`push,`** ] { **`on`** | **`off`** } **`)`**\
> **`#pragma strict_gs_check( pop )`**

## <a name="remarks"></a>Примечания

Заставляет компилятор вставлять случайные объекты cookie в стек функции, помогая обнаруживать некоторые категории переполнения буфера на основе стека. По умолчанию **`/GS`** параметр компилятора не вставляет файл cookie для всех функций. Дополнительные сведения см. в разделе [ `/GS` (проверка безопасности буфера)](../build/reference/gs-buffer-security-check.md).

Скомпилируйте с помощью, **`/GS`** чтобы включить **`strict_gs_check`** .

Используйте его pragma в модулях кода, предоставляемых потенциально опасным данным. **`strict_gs_check`** является агрессивным pragma и применяется к функциям, которые могут не нуждаться в этой защите, но оптимизированы для снижения ее воздействия на производительность результирующего приложения.

Даже при использовании этого pragma следует стремиться к написанию безопасного кода. То есть убедитесь, что в коде нет переполнения буфера. **`strict_gs_check`** может защитить приложение от переполнений буфера, которые остаются в коде.

## <a name="example"></a>Пример

В этом примере переполнение буфера возникает при копировании массива в локальный массив. При компиляции этого кода **`/GS`** в стек не вставляется файл cookie, поскольку тип данных массива является указателем. Добавление **`strict_gs_check`** pragma вызывает принудительное выполнение файла cookie стека в стеке функций.

```cpp
// pragma_strict_gs_check.cpp
// compile with: /c

#pragma strict_gs_check(on)

void ** ReverseArray(void **pData,
                     size_t cData)
{
    // **_ This buffer is subject to being overrun!! _*_
    void _pReversed[20];

    // Reverse the array into a temporary buffer
    for (size_t j = 0, i = cData; i ; --i, ++j)
        // *** Possible buffer overrun!! ***
            pReversed[j] = pData[i];

    // Copy temporary buffer back into input/output buffer
    for (size_t i = 0; i < cData ; ++i)
        pData[i] = pReversed[i];

    return pData;
}
```

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)\
[`/GS` (Проверка безопасности буфера)](../build/reference/gs-buffer-security-check.md)
