---
description: 'Дополнительные сведения: __svm_vmload'
title: __svm_vmload
ms.date: 09/02/2019
f1_keywords:
- __svm_vmload
helpviewer_keywords:
- __svm_vmload intrinsic
- VMLOAD instruction
ms.assetid: b46a5592-db76-4ffc-8694-2f3494e28bed
ms.openlocfilehash: 975f6aed50007b0b184bbab2b9b48790e5e20616
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333713"
---
# <a name="__svm_vmload"></a>__svm_vmload

**Блок, относящийся только к системам Microsoft**

Загружает подмножество состояния процессора из указанного блока управления виртуальной машиной (ВМКБ).

## <a name="syntax"></a>Синтаксис

```C
void __svm_vmload(
   size_t VmcbPhysicalAddress
);
```

### <a name="parameters"></a>Параметры

*вмкбфисикаладдресс*\
окне Физический адрес ВМКБ.

## <a name="remarks"></a>Комментарии

Функция `__svm_vmload` эквивалентна инструкции компьютера `VMLOAD` . Эта функция поддерживает взаимодействие монитора виртуальной машины узла с гостевой операционной системой и ее приложениями. Дополнительные сведения см. в документе "Ручная задача программиста архитектуры AMD64: том 2. Программирование системы", "номер документа 24593, редакция 3,11" на сайте [AMD Corporation](https://developer.amd.com/resources/developer-guides-manuals/) .

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__svm_vmload`|x86, x64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__svm_vmrun](../intrinsics/svm-vmrun.md)\
[__svm_vmsave](../intrinsics/svm-vmsave.md)
