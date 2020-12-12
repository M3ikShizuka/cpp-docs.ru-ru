---
description: 'Дополнительные сведения: __lidt'
title: __lidt
ms.date: 09/02/2019
f1_keywords:
- __lidt
- __lidt_cpp
helpviewer_keywords:
- LIDT instruction
- __lidt intrinsic
ms.assetid: 8298d25d-a19e-4900-828d-6b3b09841882
ms.openlocfilehash: 9b9f4bc51bab07a578671932c16548a0a49d155b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97167777"
---
# <a name="__lidt"></a>__lidt

**Блок, относящийся только к системам Microsoft**

Загружает регистр таблицы дескрипторов прерываний (ИДТР) со значением в указанном расположении в памяти.

## <a name="syntax"></a>Синтаксис

```C
void __lidt(void * Source);
```

### <a name="parameters"></a>Параметры

*Источника*\
окне Указатель на значение, которое должно быть скопировано в ИДТР.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__lidt`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

`__lidt`Функция эквивалентна `LIDT` инструкции компьютера и доступна только в режиме ядра. Дополнительные сведения см. в документе "Руководство разработчика по архитектуры Intel, том 2. Справочник по набору инструкций" на сайте корпорации [Intel](https://software.intel.com/articles/intel-sdm) .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__sidt](../intrinsics/sidt.md)
