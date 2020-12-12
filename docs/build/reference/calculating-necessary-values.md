---
description: 'Дополнительные сведения: вычисление необходимых значений'
title: Вычисление необходимых значений
ms.date: 11/04/2016
helpviewer_keywords:
- helper functions, calculating necessary values
ms.assetid: 4f037d0f-881a-4a48-a9d2-9f8872dfccb7
ms.openlocfilehash: 92d8462be2db55dbc10375629b133d9286560878
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97179347"
---
# <a name="calculating-necessary-values"></a>Вычисление необходимых значений

Две важные части информации должны рассчитываться с помощью вспомогательной подпрограммы Delay. Для этого в делайхлп. cpp есть две встроенные функции для вычисления этой информации.

- Сначала вычисляет индекс текущего импорта в трех различных таблицах (импорт таблицы адресов (IAT), связанную таблицу адресов импорта (Биат) и несвязанную таблицу адресов импорта (УИАТ)).

- Вторая подсчитывает количество импортов в допустимой IAT.

```cpp
// utility function for calculating the index of the current import
// for all the tables (INT, BIAT, UIAT, and IAT).
__inline unsigned
IndexFromPImgThunkData(PCImgThunkData pitdCur, PCImgThunkData pitdBase) {
    return pitdCur - pitdBase;
    }

// utility function for calculating the count of imports given the base
// of the IAT. NB: this only works on a valid IAT!
__inline unsigned
CountOfImports(PCImgThunkData pitdBase) {
    unsigned        cRet = 0;
    PCImgThunkData  pitd = pitdBase;
    while (pitd->u1.Function) {
        pitd++;
        cRet++;
        }
    return cRet;
    }
```

## <a name="see-also"></a>См. также раздел

[Основные сведения о вспомогательной функции](understanding-the-helper-function.md)
