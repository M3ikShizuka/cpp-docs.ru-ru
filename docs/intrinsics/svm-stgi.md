---
description: 'Дополнительные сведения: __svm_stgi'
title: __svm_stgi
ms.date: 09/02/2019
f1_keywords:
- __svm_stgi
helpviewer_keywords:
- __svm_stgi intrinsic
- STGI instruction
ms.assetid: 96488da4-5587-4e99-8674-627a9e51be84
ms.openlocfilehash: 8a6c7c221ed0bbf71a00685e8a0545818dd507a1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97336851"
---
# <a name="__svm_stgi"></a>__svm_stgi

**Блок, относящийся только к системам Microsoft**

Задает глобальный флаг прерывания.

## <a name="syntax"></a>Синтаксис

```C
void __svm_stgi(void);
```

## <a name="remarks"></a>Remarks

Функция `__svm_stgi` эквивалентна инструкции компьютера `STGI` . Глобальный флаг прерывания определяет, будет ли микропроцессор игнорировать, откладывать или обрабатывать прерывания из-за таких событий, как завершение ввода-вывода, предупреждение о температуре оборудования или исключение отладки.

Эта функция поддерживает взаимодействие монитора виртуальной машины узла с гостевой операционной системой и ее приложениями. Чтобы получить дополнительные сведения, выполните поиск по фразе "ручное выполнение кода программиста архитектуры AMD64 2: Системное программирование" на сайте [AMD Corporation](https://developer.amd.com/resources/developer-guides-manuals/) .

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__svm_stgi`|x86, x64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__svm_clgi](../intrinsics/svm-clgi.md)
