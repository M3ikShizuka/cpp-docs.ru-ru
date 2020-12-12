---
description: 'Дополнительные сведения о: high_resolution_clock struct'
title: Структура high_resolution_clock | Документация Майкрософт
ms.custom: ''
ms.date: 05/22/2018
ms.technology: cpp-standard-libraries
ms.topic: reference
f1_keywords:
- chrono/std::chrono::high_resolution_clock
dev_langs:
- C++
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2c5272413636e40dadf9201f684d32aaaa6708ac
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324058"
---
# <a name="high_resolution_clock-struct"></a>Структура high_resolution_clock

Представляет *high_resolution* часы.

## <a name="syntax"></a>Синтаксис

```cpp
class high_resolution_clock
```

## <a name="members"></a>Члены

### <a name="typedefs"></a>Определения типов

|Имя|Описание|
|----------|-----------------|
|`duration`|Синоним `nanoseconds` , определенный в \<chrono> .|
|`period`|Синоним `nano` , определенный в \<ratio> .|
|`rep`|Синоним **`long long`** типа, который используется для представления количества тактов часов в автономном экземпляре `duration` .|
|`time_point`|Синоним для `chrono::time_point<high_resolution_clock>`.|

## <a name="functions"></a>Функции

|Имя|Описание|
|-|-|
|`now`|Возвращает текущее время в виде `time_point` значения.|

## <a name="constants"></a>Константы

|Имя|Описание|
|----------|-----------------|
|`is_steady`|Содержит **`true`** . Объект `high_resolution_clock` — *постоянный*.|
