---
description: 'Дополнительные сведения: __vmx_vmptrld'
title: __vmx_vmptrld
ms.date: 09/02/2019
f1_keywords:
- __vmx_vmptrld
helpviewer_keywords:
- __vmx_vmptrld intrinsic
- VMPTRLD instruction
ms.assetid: 95c9ec5b-1a81-41ba-983e-327bd6a65fcb
ms.openlocfilehash: 850311e4423940ebd34a203e6d43ec961b3258f4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333532"
---
# <a name="__vmx_vmptrld"></a>__vmx_vmptrld

**Блок, относящийся только к системам Microsoft**

Загружает указатель на текущую структуру управления виртуальными машинами (VMCS) по указанному адресу.

## <a name="syntax"></a>Синтаксис

```C
int __vmx_vmptrld(
   unsigned __int64 *VmcsPhysicalAddress
);
```

### <a name="parameters"></a>Параметры

*вмксфисикаладдресс*\
окне Адрес, по которому хранится указатель VMCS.

## <a name="return-value"></a>Возвращаемое значение

0,0
Операция успешно выполнена.

одного
Не удалось выполнить операцию; расширенные сведения о состоянии доступны в `VM-instruction error field` текущей структуре VMCS.

открыт
Сбой операции без сведений о состоянии.

## <a name="remarks"></a>Комментарии

Указатель VMCS — это 64-разрядный физический адрес.

Функция `__vmx_vmptrld` эквивалентна инструкции компьютера `VMPTRLD` . Эта функция поддерживает взаимодействие монитора виртуальной машины узла с гостевой операционной системой и ее приложениями. Дополнительные сведения см. в документе "Техническая спецификация виртуализации Intel для архитектуры IA-32 Intel" номер документа C97063-002 на сайте корпорации [Intel](https://software.intel.com/articles/intel-sdm) .

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__vmx_vmptrld`|X64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__vmx_vmptrst](../intrinsics/vmx-vmptrst.md)
