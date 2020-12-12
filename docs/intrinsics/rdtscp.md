---
description: 'Дополнительные сведения: __rdtscp'
title: __rdtscp
ms.date: 09/02/2019
f1_keywords:
- __rdtscp
helpviewer_keywords:
- rdtscp intrinsic
- __rdtscp intrinsic
- rdtscp instruction
ms.assetid: f17d9a9c-88bb-44e0-b69d-d516bc1c93ee
ms.openlocfilehash: 511d0f1001c218fd838d4bb315fe8c95f10eb3bf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97257499"
---
# <a name="__rdtscp"></a>__rdtscp

**Блок, относящийся только к системам Microsoft**

Формирует `rdtscp` инструкцию, выполняет запись `TSC_AUX[31:0` ] в память и возвращает счетчик 64-битной метки времени ( `TSC)` результат.

## <a name="syntax"></a>Синтаксис

```C
unsigned __int64 __rdtscp(
   unsigned int * AUX
);
```

### <a name="parameters"></a>Параметры

*ДОПОЛНИТЕЛЬНЫЙ*\
заполняет Указатель на расположение, которое будет содержать содержимое регистра, зависящего от компьютера `TSC_AUX[31:0]` .

## <a name="return-value"></a>Возвращаемое значение

Число тактов 64-битового целого числа без знака.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__rdtscp`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

`__rdtscp`Внутренняя функция создает `rdtscp` инструкцию. Чтобы определить аппаратную поддержку для этой инструкции, вызовите `__cpuid` встроенную функцию с `InfoType=0x80000001` и проверьте бит 27 из `CPUInfo[3] (EDX)` . Этот бит равен 1, если инструкция поддерживается, и 0 в противном случае.  Если запустить код, использующий встроенное на оборудовании, которое не поддерживает эту `rdtscp` инструкцию, результаты будут непредсказуемыми.

Эта инструкция ожидает, пока все предыдущие инструкции не будут выполнены и все предыдущие выявляются глобально видимыми. Однако это не инструкция сериализации. Дополнительные сведения см. в руководствах по Intel и AMD.

Значение в `TSC_AUX[31:0]` зависит от операционной системы.

## <a name="example"></a>Пример

```cpp
#include <intrin.h>
#include <stdio.h>
int main()
{
    unsigned __int64 i;
    unsigned int ui;
    i = __rdtscp(&ui);
    printf_s("%I64d ticks\n", i);
    printf_s("TSC_AUX was %x\n", ui);
}
```

```Output
3363423610155519 ticks
TSC_AUX was 0
```

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[__rdtsc](../intrinsics/rdtsc.md)\
[Встроенные объекты компилятора](../intrinsics/compiler-intrinsics.md)
