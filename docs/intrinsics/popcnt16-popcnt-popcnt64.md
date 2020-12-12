---
description: 'Дополнительные сведения: __popcnt16, __popcnt, __popcnt64'
title: __popcnt16, __popcnt, __popcnt64
ms.date: 09/02/2019
f1_keywords:
- __popcnt64
- __popcnt
- __popcnt16
helpviewer_keywords:
- popcnt instruction
- __popcnt16
- __popcnt64
- __popcnt
ms.assetid: e525b236-adc8-42df-9b9b-8b7d8c245d3b
ms.openlocfilehash: cb95ff09d589cfd9a9cfc438d0334cf68f073825
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97257528"
---
# <a name="__popcnt16-__popcnt-__popcnt64"></a>__popcnt16, __popcnt, __popcnt64

**Блок, относящийся только к системам Microsoft**

Подсчитывает количество `1` битов (число совокупностей) в 16-, 32-или 64-разрядном целом числе без знака.

## <a name="syntax"></a>Синтаксис

```C
unsigned short __popcnt16(
   unsigned short value
);
unsigned int __popcnt(
   unsigned int value
);
unsigned __int64 __popcnt64(
   unsigned __int64 value
);
```

### <a name="parameters"></a>Параметры

*значений*\
окне 16-, 32-или 64-разрядное целое число без знака, для которого требуется получить число заполнений.

## <a name="return-value"></a>Возвращаемое значение

Число `1` битов в параметре *value* .

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__popcnt16`|Расширенная обработка битов|
|`__popcnt`|Расширенная обработка битов|
|`__popcnt64`|Расширенная обработка битов в 64-разрядном режиме.|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Каждая из встроенных функций формирует `popcnt` инструкцию. В 32-разрядном режиме нет 64-битных регистров общего назначения, поэтому 64-bit `popcnt` не поддерживается.

Чтобы определить аппаратную поддержку для `popcnt` инструкции, вызовите `__cpuid` встроенную функцию с `InfoType=0x00000001` и проверьте бит 23 `CPUInfo[2] (ECX)` . Этот бит равен 1, если инструкция поддерживается, и 0 в противном случае. Если запустить код, использующий эти встроенные функции на оборудовании, не поддерживающем `popcnt` инструкцию, результаты будут непредсказуемыми.

## <a name="example"></a>Пример

```cpp
#include <iostream>
#include <intrin.h>
using namespace std;

int main()
{
  unsigned short us[3] = {0, 0xFF, 0xFFFF};
  unsigned short usr;
  unsigned int   ui[4] = {0, 0xFF, 0xFFFF, 0xFFFFFFFF};
  unsigned int   uir;

  for (int i=0; i<3; i++) {
    usr = __popcnt16(us[i]);
    cout << "__popcnt16(0x" << hex << us[i] << ") = " << dec << usr << endl;
  }

  for (int i=0; i<4; i++) {
    uir = __popcnt(ui[i]);
    cout << "__popcnt(0x" << hex << ui[i] << ") = " << dec << uir << endl;
  }
}
```

```Output
__popcnt16(0x0) = 0
__popcnt16(0xff) = 8
__popcnt16(0xffff) = 16
__popcnt(0x0) = 0
__popcnt(0xff) = 8
__popcnt(0xffff) = 16
__popcnt(0xffffffff) = 32
```

**Завершение блока, относящегося только к системам Майкрософт**

Для частей авторские права на 2007 по расширенным микроустройствам, Inc. Все права защищены. Воспроизводить с разрешением от расширенных микроустройств, Inc.

## <a name="see-also"></a>См. также раздел

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
