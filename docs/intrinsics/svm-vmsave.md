---
description: 'Дополнительные сведения: __svm_vmsave'
title: __svm_vmsave
ms.date: 09/02/2019
f1_keywords:
- __svm_vmsave
helpviewer_keywords:
- VMSAVE instruction
- __svm_vmsave intrinsic
ms.assetid: 617a60bd-8514-4ba1-8066-bcf4dd481030
ms.openlocfilehash: 5c0e4eb5f2d4c0f73921572811b070c8f87a2673
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333682"
---
# <a name="__svm_vmsave"></a>__svm_vmsave

**Блок, относящийся только к системам Microsoft**

Сохраняет подмножество состояния процессора в указанном блоке управления виртуальной машиной (ВМКБ).

## <a name="syntax"></a>Синтаксис

```C
void __svm_vmsave(
   size_t VmcbPhysicalAddress
);
```

### <a name="parameters"></a>Параметры

*вмкбфисикаладдресс*\
окне Физический адрес ВМКБ.

## <a name="remarks"></a>Комментарии

Функция `__svm_vmsave` эквивалентна инструкции компьютера `VMSAVE` . Эта функция поддерживает взаимодействие монитора виртуальной машины узла с гостевой операционной системой и ее приложениями. Дополнительные сведения см. в документе "Ручная задача программиста архитектуры AMD64, том 2. Программирование системы", "номер документа 24593, редакция 3,11 или более поздней версии" на сайте [AMD Corporation](https://developer.amd.com/resources/developer-guides-manuals/) .

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__svm_vmsave`|x86, x64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__svm_vmrun](../intrinsics/svm-vmrun.md)\
[__svm_vmload](../intrinsics/svm-vmload.md)
