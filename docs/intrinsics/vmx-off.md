---
description: 'Дополнительные сведения: __vmx_off'
title: __vmx_off
ms.date: 09/02/2019
f1_keywords:
- __vmx_off
helpviewer_keywords:
- VMXOFF instruction
- __vmx_off intrinsic
ms.assetid: 78a32d46-9291-406c-b982-a550855aff18
ms.openlocfilehash: d36b9079165dd68b207658d6141bdf11bd9747cb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333582"
---
# <a name="__vmx_off"></a>__vmx_off

**Блок, относящийся только к системам Microsoft**

Деактивирует операцию расширения виртуальной машины (VMX) в процессоре.

## <a name="syntax"></a>Синтаксис

```C
void __vmx_off();
```

## <a name="remarks"></a>Remarks

Функция `__vmx_off` эквивалентна инструкции компьютера `VMXOFF` . Эта функция поддерживает взаимодействие монитора виртуальной машины узла с гостевой операционной системой и ее приложениями. Дополнительные сведения см. в документе "Техническая спецификация виртуализации Intel для архитектуры IA-32 Intel" номер документа C97063-002 на сайте корпорации [Intel](https://software.intel.com/articles/intel-sdm) .

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__vmx_off`|x86, x64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
