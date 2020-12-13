---
description: 'Дополнительные сведения: __svm_vmrun'
title: __svm_vmrun
ms.date: 09/02/2019
f1_keywords:
- __svm_vmrun
helpviewer_keywords:
- __svm_vmrun intrinsic
- VMRUN instruction
ms.assetid: ae98a781-fc17-47b2-b40f-86fcebf1867b
ms.openlocfilehash: c01716e496513aa11132fdfc95235a39c7277279
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333695"
---
# <a name="__svm_vmrun"></a>__svm_vmrun

**Блок, относящийся только к системам Microsoft**

Запускает выполнение гостевого кода виртуальной машины, соответствующего указанному блоку управления виртуальной машиной (ВМКБ).

## <a name="syntax"></a>Синтаксис

```C
void __svm_vmrun(
   size_t VmcbPhysicalAddress
);
```

### <a name="parameters"></a>Параметры

*вмкбфисикаладдресс*\
окне Физический адрес ВМКБ.

## <a name="remarks"></a>Комментарии

`__svm_vmrun`Функция использует минимальный объем информации в вмкб, чтобы начать выполнять гостевой код виртуальной машины. Используйте функцию [__svm_vmsave](../intrinsics/svm-vmsave.md) или [__svm_vmload](../intrinsics/svm-vmload.md) , если требуются дополнительные сведения для обработки сложного прерывания или переключения на другой гость.

Функция `__svm_vmrun` эквивалентна инструкции компьютера `VMRUN` . Эта функция поддерживает взаимодействие монитора виртуальной машины узла с гостевой операционной системой и ее приложениями. Дополнительные сведения см. в документе "Ручная задача программиста архитектуры AMD64, том 2. Программирование системы", "номер документа 24593, редакция 3,11 или более поздней версии" на сайте [AMD Corporation](https://developer.amd.com/resources/developer-guides-manuals/) .

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__svm_vmrun`|x86, x64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__svm_vmsave](../intrinsics/svm-vmsave.md)\
[__svm_vmload](../intrinsics/svm-vmload.md)
