---
description: 'Дополнительные сведения: __halt'
title: __halt
ms.date: 09/02/2019
f1_keywords:
- __halt
- __halt_cpp
helpviewer_keywords:
- __halt intrinsic
- HLT instruction
ms.assetid: a074f44a-101c-45a5-8a5e-cfd223c34002
ms.openlocfilehash: e38478b14b59c910e6d6ac12f9cb69fa369e3459
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336982"
---
# <a name="__halt"></a>__halt

**Блок, относящийся только к системам Microsoft**

Прерывает работу микропроцессора до включенного прерывания, немаскированного прерывания (NMI) или сброса.

## <a name="syntax"></a>Синтаксис

```C
void __halt( void );
```

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__halt`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

`__halt`Функция эквивалентна `HLT` инструкции компьютера и доступна только в режиме ядра. Дополнительные сведения см. в документе "Руководство разработчика по архитектуры Intel, том 2. Справочник по набору инструкций" на сайте корпорации [Intel](https://software.intel.com/articles/intel-sdm) .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
