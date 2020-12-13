---
description: 'Дополнительные сведения: __vmx_on'
title: __vmx_on
ms.date: 09/02/2019
f1_keywords:
- __vmx_on
helpviewer_keywords:
- VMXON instruction
- __vmx_on intrinsic
ms.assetid: 16804991-6a75-4adf-8ec2-bc95acfa4801
ms.openlocfilehash: a1e9171fe64a239b592f0d27ec49d4159b46523d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333579"
---
# <a name="__vmx_on"></a>__vmx_on

**Блок, относящийся только к системам Microsoft**

Активирует операцию расширения виртуальной машины (VMX) в процессоре.

## <a name="syntax"></a>Синтаксис

```C
unsigned char __vmx_on(
   unsigned __int64 *VmsSupportPhysicalAddress
);
```

### <a name="parameters"></a>Параметры

*вмссуппортфисикаладдресс*\
окне Указатель на 64-разрядный физический адрес, указывающий на структуру управления виртуальными машинами (VMCS).

## <a name="return-value"></a>Возвращаемое значение

|Значение|Значение|
|-----------|-------------|
|0|Операция успешно выполнена.|
|1|Не удалось выполнить операцию; расширенные сведения о состоянии доступны в `VM-instruction error field` текущей структуре VMCS.|
|2|Сбой операции без сведений о состоянии.|

## <a name="remarks"></a>Комментарии

`__vmx_on`Функция соответствует `VMXON` инструкции компьютера. Эта функция поддерживает взаимодействие монитора виртуальной машины узла с гостевой операционной системой и ее приложениями. Дополнительные сведения см. в документе "Техническая спецификация виртуализации Intel для архитектуры IA-32 Intel" номер документа C97063-002 на сайте корпорации [Intel](https://software.intel.com/articles/intel-sdm) .

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__vmx_on`|X64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
