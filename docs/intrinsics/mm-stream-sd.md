---
description: 'Дополнительные сведения: _mm_stream_sd'
title: _mm_stream_sd
ms.date: 09/02/2019
f1_keywords:
- _mm_stream_sd
helpviewer_keywords:
- _mm_stream_sd intrinsic
- movntsd instruction
ms.assetid: 2b4bea5e-e64e-45fa-9afc-88a2e4b82cfc
ms.openlocfilehash: 60ef13afcbe99e1390f4eb1087fddc5540a7de34
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97133267"
---
# <a name="_mm_stream_sd"></a>_mm_stream_sd

**Блок, относящийся только к системам Microsoft**

Записывает 64-битные данные в расположение в памяти, не замусоривать кэши.

## <a name="syntax"></a>Синтаксис

```C
void _mm_stream_sd(
   double * Dest,
   __m128d Source
);
```

### <a name="parameters"></a>Параметры

*Dest*\
заполняет Указатель на расположение, в которое будут записываться исходные данные.

*Источника*\
окне 128-разрядное значение, содержащее **`double`** значение, записываемое в последние 64 бит.

## <a name="return-value"></a>Возвращаемое значение

Отсутствует.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`_mm_stream_sd`|SSE4a|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Внутренняя функция создает `movntsd` инструкцию. Чтобы определить поддержку оборудования для этой инструкции, вызовите `__cpuid` встроенную функцию с параметром `InfoType=0x80000001` и установите бит 6 из `CPUInfo[2] (ECX)` . Этот бит равен 1, если оборудование поддерживает эту инструкцию, и 0 в противном случае.

Если запустить код, использующий `_mm_stream_sd` встроенное на оборудовании, которое не поддерживает эту `movntsd` инструкцию, результаты будут непредсказуемыми.

## <a name="example"></a>Пример

```cpp
// Compile this sample with: /EHsc
#include <iostream>
#include <intrin.h>
using namespace std;

int main()
{
    __m128d vals;
    double d[2];

    d[0] = -1.;
    d[1] = -2.;
    vals.m128d_f64[0] = 0.;
    vals.m128d_f64[1] = 1.;
    _mm_stream_sd(&d[1], vals);
    cout << "d[0] = " << d[0] << ", d[1] = " << d[1] << endl;
}
```

```Output
d[0] = -1, d[1] = 1
```

**Завершение блока, относящегося только к системам Майкрософт**

Для частей авторские права на 2007 по расширенным микроустройствам, Inc. Все права защищены. Воспроизводить с разрешением от расширенных микроустройств, Inc.

## <a name="see-also"></a>См. также раздел

[_mm_stream_ss](../intrinsics/mm-stream-ss.md)\
[_mm_store_sd](https://software.intel.com/sites/landingpage/IntrinsicsGuide/#text=_mm_store_sd)\
[_mm_sfence](https://software.intel.com/sites/landingpage/IntrinsicsGuide/#text=_mm_sfence)\
[Встроенные объекты компилятора](../intrinsics/compiler-intrinsics.md)
