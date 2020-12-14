---
description: 'Дополнительные сведения: __svm_invlpga'
title: __svm_invlpga
ms.date: 09/02/2019
f1_keywords:
- __svm_invlpga
helpviewer_keywords:
- __svm_invlpga intrinsic
- INVLPGA instruction
ms.assetid: aa6578ce-8278-464b-8815-a0fc45330915
ms.openlocfilehash: dc976f535381fcfdfec0da5c1a280c4df281c114
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97314754"
---
# <a name="__svm_invlpga"></a>__svm_invlpga

**Блок, относящийся только к системам Microsoft**

Делает недействительным запись сопоставления адресов в буфере переноса компьютера. Параметры укажите виртуальный адрес и идентификатор пространства адресов страницы, которые необходимо сделать недействительными.

## <a name="syntax"></a>Синтаксис

```C
void __svm_invlpga(void *Vaddr, int as_id);
```

### <a name="parameters"></a>Параметры

*ваддр*\
окне Виртуальный адрес страницы, которую необходимо сделать недействительной.

*as_id*\
окне Идентификатор адресного пространства (асид) страницы, которую необходимо сделать недействительной.

## <a name="remarks"></a>Комментарии

Функция `__svm_invlpga` эквивалентна инструкции компьютера `INVLPGA` . Эта функция поддерживает взаимодействие монитора виртуальной машины узла с гостевой операционной системой и ее приложениями. Дополнительные сведения см. в документе "Ручная задача программиста архитектуры AMD64: том 2. Программирование системы", "номер документа 24593, редакция 3,11" на сайте [AMD Corporation](https://developer.amd.com/resources/developer-guides-manuals/) .

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__svm_invlpga`|x86, x64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
