---
description: 'Дополнительные сведения: __svm_clgi'
title: __svm_clgi
ms.date: 09/02/2019
f1_keywords:
- __svm_clgi
helpviewer_keywords:
- CLGI instruction
- __svm_clgi intrinsic
ms.assetid: 6640f5ab-9472-46f9-a042-e15c4f1ff858
ms.openlocfilehash: d0b372e28b0b119d3576dd87b34f1edf883f1337
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336867"
---
# <a name="__svm_clgi"></a>__svm_clgi

**Блок, относящийся только к системам Microsoft**

Очищает глобальный флаг прерывания.

## <a name="syntax"></a>Синтаксис

```C
void __svm_clgi( void );
```

## <a name="remarks"></a>Remarks

Функция `__svm_clgi` эквивалентна инструкции компьютера `CLGI` . Глобальный флаг прерывания определяет, будет ли микропроцессор игнорировать, откладывать или обрабатывать прерывания из-за таких событий, как завершение ввода-вывода, предупреждение о температуре оборудования или исключение отладки.

Эта функция поддерживает взаимодействие монитора виртуальной машины узла с гостевой операционной системой и ее приложениями. Чтобы получить дополнительные сведения, выполните поиск по фразе "ручное выполнение кода программиста архитектуры AMD64 2: Системное программирование" на сайте [AMD Corporation](https://developer.amd.com/resources/developer-guides-manuals/) .

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__svm_clgi`|x86, x64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__svm_stgi](../intrinsics/svm-stgi.md)
