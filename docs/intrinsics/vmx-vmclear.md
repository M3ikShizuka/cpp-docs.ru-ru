---
description: 'Дополнительные сведения: __vmx_vmclear'
title: __vmx_vmclear
ms.date: 09/02/2019
f1_keywords:
- __vmx_vmclear
helpviewer_keywords:
- VMCLEAR instruction
- __vmx_vmclear intrinsic
ms.assetid: e3eb98e4-50fc-4c93-9bac-340fd1f0a466
ms.openlocfilehash: 2eec5c1189c6a798246a6dabfc731fb0166bc14a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333556"
---
# <a name="__vmx_vmclear"></a>__vmx_vmclear

**Блок, относящийся только к системам Microsoft**

Инициализирует указанную структуру управления виртуальными машинами (VMCS) и задает для ее состояния запуска значение `Clear` .

## <a name="syntax"></a>Синтаксис

```C
unsigned char __vmx_vmclear(
   unsigned __int64 *VmcsPhysicalAddress
);
```

### <a name="parameters"></a>Параметры

*вмксфисикаладдресс*\
окне Указатель на 64-разрядное расположение в памяти, которое содержит физический адрес VMCS для очистки.

## <a name="return-value"></a>Возвращаемое значение

|Значение|Значение|
|-----------|-------------|
|0|Операция успешно выполнена.|
|1|Не удалось выполнить операцию; расширенные сведения о состоянии доступны в `VM-instruction error field` текущей структуре VMCS.|
|2|Сбой операции без сведений о состоянии.|

## <a name="remarks"></a>Комментарии

Приложение может выполнить операцию типа "виртуальная машина — ввод" с помощью функции [__vmx_vmlaunch](../intrinsics/vmx-vmlaunch.md) или [__vmx_vmresume](../intrinsics/vmx-vmresume.md) . Функция [__vmx_vmlaunch](../intrinsics/vmx-vmlaunch.md) может использоваться только с VMCS, состояние запуска которого равно `Clear` , а функция [__vmx_vmresume](../intrinsics/vmx-vmresume.md) может использоваться только с VMCS, состояние запуска которого — `Launched` . Следовательно, используйте функцию [__vmx_vmclear](../intrinsics/vmx-vmclear.md) , чтобы установить состояние запуска VMCS на `Clear` . Используйте функцию [__vmx_vmlaunch](../intrinsics/vmx-vmlaunch.md) для первой операции ввода виртуальной машины и функции [__vmx_vmresume](../intrinsics/vmx-vmresume.md) для ПОСЛЕДУЮЩЕЙ операции ввода виртуальной машины.

Функция `__vmx_vmclear` эквивалентна инструкции компьютера `VMCLEAR` . Эта функция поддерживает взаимодействие монитора виртуальной машины узла с гостевой операционной системой и ее приложениями. Дополнительные сведения см. в документе "Техническая спецификация виртуализации Intel для архитектуры IA-32 Intel" номер документа C97063-002 на сайте корпорации [Intel](https://software.intel.com/articles/intel-sdm) .

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__vmx_vmclear`|X64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__vmx_vmlaunch](../intrinsics/vmx-vmlaunch.md)\
[__vmx_vmresume](../intrinsics/vmx-vmresume.md)
