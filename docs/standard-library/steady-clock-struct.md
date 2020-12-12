---
description: 'Дополнительные сведения о: steady_clock struct'
title: Структура steady_clock
ms.date: 05/22/2018
f1_keywords:
- chrono/std::chrono::steady_clock
ms.assetid: 970d12ec-fc80-4391-a2f7-b57b2aec668d
ms.openlocfilehash: 066a98f4eba6670e640e9fcc9b79eb017859a3d2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97169077"
---
# <a name="steady_clock-struct"></a>Структура steady_clock

Представляет *устойчивые* часы.

## <a name="syntax"></a>Синтаксис

```cpp
struct steady_clock;
```

## <a name="remarks"></a>Remarks

В Windows `steady_clock` заключает в оболочку `QueryPerformanceCounter` функцию.

Часы считаются *монотонными*, если значение, возвращаемое при первом вызове `now`, всегда не больше значений, возвращаемых при последующих вызовах `now`. Часы считаются *постоянными*, если они *монотонны* и интервал времени между соседними тактами является постоянной величиной.

`high_resolution_clock` является typedef для `steady_clock` .

### <a name="public-typedefs"></a>Открытые определения типов

|Имя|Описание|
|----------|-----------------|
|`steady_clock::duration`|Синоним `nanoseconds` , определенный в \<chrono> .|
|`steady_clock::period`|Синоним `nano` , определенный в \<ratio> .|
|`steady_clock::rep`|Синоним **`long long`** типа, который используется для представления количества тактов часов в автономном экземпляре `duration` .|
|`steady_clock::time_point`|Синоним для `chrono::time_point<steady_clock>`.|

## <a name="public-functions"></a>Открытые функции

|Функция|Описание|
|--------------|-----------------|
|`now`|Возвращает текущее время в виде `time_point` значения.|

## <a name="public-constants"></a>Открытые константы

|Имя|Описание|
|----------|-----------------|
|`steady_clock::is_steady`|Содержит **`true`** . Объект `steady_clock` — *постоянный*.|

## <a name="requirements"></a>Требования

**Заголовок:**\<chrono>

**Пространство имен:** std::chrono

## <a name="see-also"></a>См. также раздел

- [Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)
- [\<chrono>](../standard-library/chrono.md)
- [Структура system_clock](../standard-library/system-clock-structure.md)
