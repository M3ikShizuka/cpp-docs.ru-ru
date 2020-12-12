---
description: 'Дополнительные сведения: __sidt'
title: __sidt
ms.date: 09/02/2019
f1_keywords:
- __sidt
helpviewer_keywords:
- sidt instruction
- __sidt intrinsic
ms.assetid: 01e83d14-6e63-4dea-8f64-5a0339d69641
ms.openlocfilehash: 075351bc10981dd8453381e9ce9393a046dfd884
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97306967"
---
# <a name="__sidt"></a>__sidt

**Блок, относящийся только к системам Microsoft**

Сохраняет значение регистра таблицы дескрипторов прерываний (ИДТР) в указанном расположении в памяти.

## <a name="syntax"></a>Синтаксис

```C
void __sidt(void * Destination);
```

### <a name="parameters"></a>Параметры

*Местоназначение*\
окне Указатель на место в памяти, где хранится ИДТР.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__sidt`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Функция `__sidt` эквивалентна инструкции компьютера `SIDT` . Дополнительные сведения см. в документе "Руководство разработчика по архитектуры Intel, том 2. Справочник по набору инструкций" на сайте корпорации [Intel](https://software.intel.com/articles/intel-sdm) .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__lidt](../intrinsics/lidt.md)
