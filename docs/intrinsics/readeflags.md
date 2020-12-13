---
description: 'Дополнительные сведения: __readeflags'
title: __readeflags
ms.date: 09/02/2019
f1_keywords:
- __readeflags
helpviewer_keywords:
- __readeflags intrinsic
ms.assetid: f9d2f4d8-c428-491f-b8de-04d0566b2b6b
ms.openlocfilehash: e74864f522ba411f44b4a264e9c0e1fd16aa84ee
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97341000"
---
# <a name="__readeflags"></a>__readeflags

**Блок, относящийся только к системам Microsoft**

Считывает Регистр состояния программы и управления (ЕФЛАГС).

## <a name="syntax"></a>Синтаксис

```C
unsigned     int __readeflags(void); /* x86 */
unsigned __int64 __readeflags(void); /* x64 */
```

## <a name="return-value"></a>Возвращаемое значение

Значение регистра ЕФЛАГС. Возвращаемое значение — 32 бит на 32-разрядной платформе и 64 бит на 64-разрядной платформе.

## <a name="remarks"></a>Комментарии

Эти подпрограммы доступны только в виде встроенных функций.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__readeflags`|x86, x64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__writeeflags](../intrinsics/writeeflags.md)
