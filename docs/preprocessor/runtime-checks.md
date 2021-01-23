---
description: Дополнительные сведения об pragma директиве runtime_checks в Microsoft C/C++
title: runtime_checks pragma
ms.date: 01/22/2021
f1_keywords:
- vc-pragma.runtime_checks
- runtime_checks_CPP
helpviewer_keywords:
- runtime_checks pragma
- pragma, runtime_checks
no-loc:
- pragma
ms.openlocfilehash: 4932126ffe33d2f8a99f6d94e3c58d2c0322df92
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98712821"
---
# <a name="runtime_checks-no-locpragma"></a>`runtime_checks` pragma

Отключает или восстанавливает [`/RTC`](../build/reference/rtc-run-time-error-checks.md) настройки параметров компилятора.

## <a name="syntax"></a>Синтаксис

> **`#pragma runtime_checks( "`** [ *Среда выполнения-проверка-параметры* ] **`",`** { **`restore`** | **`off`** } **`)`**

## <a name="remarks"></a>Примечания

Нельзя включить проверку времени выполнения, которая не была включена параметром компилятора. Например, если не указать **`/RTCs`** в командной строке, при указании параметра `#pragma runtime_checks( "s", restore)` не будет включена проверка кадра стека.

Объект **`runtime_checks`** pragma должен находиться за пределами функции и вступает в силу при первой функции, определенной после появления pragma . **`restore`** Аргументы и **`off`** включают параметры, указанные в параметре **`runtime_checks`** pragma On или OFF.

*Параметры проверки среды выполнения* могут быть равны нулю или большему числу параметров, приведенных в следующей таблице.

### <a name="parameters-of-the-runtime_checks-pragma"></a>Параметры директивы pragma runtime_checks

| Параметры | Тип проверки времени выполнения |
|--------------------|-----------------------------|
| **`s`** | Включает проверку (кадра) стека. |
| **`c`** | Сообщает, когда значение назначается меньшему типу данных, что приводит к потере данных. |
| **`u`** | Сообщает об использовании переменной перед ее определением. |

Эти параметры являются теми же, которые используются с **`/RTC`** параметром компилятора. Например:

```cpp
#pragma runtime_checks( "sc", restore )
```

Использование **`runtime_checks`** pragma с пустой строкой ( **`""`** ) является особой формой директивы:

- При использовании **`off`** параметра происходит включение проверок ошибок во время выполнения, перечисленных в приведенной выше таблице.

- При использовании **`restore`** параметра он сбрасывает проверки ошибок во время выполнения до тех, которые были указаны с помощью **`/RTC`** параметра компилятора.

```cpp
#pragma runtime_checks( "", off )
/* runtime checks are off in this region */
#pragma runtime_checks( "", restore )
```

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
