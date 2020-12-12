---
description: 'Дополнительные сведения: _mm_extract_si64, _mm_extracti_si64'
title: _mm_extract_si64, _mm_extracti_si64
ms.date: 09/02/2019
f1_keywords:
- _mm_extracti_si64
- _mm_extract_si64
helpviewer_keywords:
- extrq instruction
- _mm_extracti_si64 intrinsic
- _mm_extract_si64 intrinsic
ms.assetid: 459fdd72-cc54-4ee5-bbd5-d2c6067a88e7
ms.openlocfilehash: 39a07c7310727de8d752c060c3d38481469ff1a7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97322871"
---
# <a name="_mm_extract_si64-_mm_extracti_si64"></a>_mm_extract_si64, _mm_extracti_si64

**Блок, относящийся только к системам Microsoft**

Формирует `extrq` инструкцию для извлечения указанных битов из младших 64 бит первого аргумента.

## <a name="syntax"></a>Синтаксис

```C
__m128i _mm_extract_si64(
   __m128i Source,
   __m128i Descriptor
);
__m128i _mm_extracti_si64(
   __m128i Source,
   int Length,
   int Index
);
```

### <a name="parameters"></a>Параметры

*Источника*\
окне 128-битовое поле с входными данными в младших 64 битах.

*Descriptor*\
окне 128-битовое поле, описывающее битовое поле для извлечения.

*Недопустим*\
окне Целое число, указывающее длину поля для извлечения.

*Номер*\
окне Целое число, указывающее индекс поля для извлечения

## <a name="return-value"></a>Возвращаемое значение

128-битовое поле с извлеченным полем в его минимально значимых битах.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`_mm_extract_si64`|SSE4a|
|`_mm_extracti_si64`|SSE4a|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эти встроенные функции создают `extrq` инструкцию для извлечения битов из *источника*. Существует две версии: `_mm_extracti_si64` это `_mm_extract_si64` немедленная версия. Каждая версия извлекает из *источника* битовое поле, определяемое его длиной, и индекс с наименьшим значащим битом. Значения длины и индекса взяты в MOD 64, поэтому обе-1 и 127 интерпретируется как 63. Если сумма (уменьшенная) индекса и (уменьшенная) Длина поля больше 64, результаты будут неопределенными. Нулевое значение для длины поля интерпретируется как 64. Если длина поля и индекс бита равны нулю, извлекается бит 63:0 *источника* . Если длина поля равна нулю, а битовый индекс не равен нулю, результаты не будут определены.

При вызове `_mm_extract_si64` *дескриптор* содержит индекс в битах 13:8 и длину поля данных, которые должны быть извлечены в битах 5:0.

При вызове `_mm_extracti_si64` с аргументами, которые компилятор не может определить как целые константы, компилятор создает код для упаковки этих значений в регистр XMM (*дескриптор*) и для вызова `_mm_extract_si64` .

Чтобы определить аппаратную поддержку для `extrq` инструкции, вызовите `__cpuid` встроенную функцию с параметром `InfoType=0x80000001` и установите бит 6 из `CPUInfo[2] (ECX)` . Этот бит будет равен 1, если инструкция поддерживается, и 0 в противном случае. Если запустить код, использующий это встроенное оборудование, которое не поддерживает эту `extrq` инструкцию, результаты будут непредсказуемыми.

## <a name="example"></a>Пример

```cpp
// Compile this sample with: /EHsc
#include <iostream>
#include <intrin.h>
using namespace std;

union {
    __m128i m;
    unsigned __int64 ui64[2];
} source, descriptor, result1, result2, result3;

int
main()
{
    source.ui64[0] =     0xfedcba9876543210ll;
    descriptor.ui64[0] = 0x0000000000000b1bll;

    result1.m = _mm_extract_si64 (source.m, descriptor.m);
    result2.m = _mm_extracti_si64(source.m, 27, 11);
    result3.ui64[0] = (source.ui64[0] >> 11) & 0x7ffffff;

    cout << hex << "result1 = 0x" << result1.ui64[0] << endl;
    cout << "result2 = 0x" << result2.ui64[0] << endl;
    cout << "result3 = 0x" << result3.ui64[0] << endl;
}
```

```Output
result1 = 0x30eca86
result2 = 0x30eca86
result3 = 0x30eca86
```

**Завершение блока, относящегося только к системам Майкрософт**

Для частей авторские права на 2007 по расширенным микроустройствам, Inc. Все права защищены. Воспроизводить с разрешением от расширенных микроустройств, Inc.

## <a name="see-also"></a>См. также раздел

[_mm_insert_si64, _mm_inserti_si64](../intrinsics/mm-insert-si64-mm-inserti-si64.md)\
[Встроенные объекты компилятора](../intrinsics/compiler-intrinsics.md)
