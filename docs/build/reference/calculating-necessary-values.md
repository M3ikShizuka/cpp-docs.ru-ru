---
description: 'Дополнительные сведения: вычисление необходимых значений для отложенной загрузки'
title: Вычисление необходимых значений для отложенной загрузки
ms.date: 01/19/2021
helpviewer_keywords:
- helper functions, calculating necessary values
ms.openlocfilehash: ae5e0c15b5b13f12fd90c1378a1e449516b55f43
ms.sourcegitcommit: 3d9cfde85df33002e3b3d7f3509ff6a8dc4c0a21
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "98667445"
---
# <a name="calculate-necessary-values-for-delay-loading"></a>Вычисление необходимых значений для отложенной загрузки

Вспомогательная подсистема с отложенной загрузкой должна вычислить два важных фрагмента информации. Чтобы вычислить эту информацию, в можно получить две встроенные функции *`delayhlp.cpp`* .

- Первый, `IndexFromPImgThunkData` ,, вычисляет индекс текущего импорта в трех различных таблицах (импорт таблицы адресов (IAT), связанную таблицу адресов импорта (Биат) и несвязанную таблицу адресов импорта (уиат)).

- Во втором, `CountOfImports` , подсчитывается количество импортов в допустимой IAT.

```C
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

[Понятие вспомогательной функции](understanding-the-helper-function.md)
