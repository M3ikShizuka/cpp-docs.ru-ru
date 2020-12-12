---
description: 'Дополнительные сведения: __invlpg'
title: __invlpg
ms.date: 09/02/2019
f1_keywords:
- __invlpg
- __invlpg_cpp
helpviewer_keywords:
- invlpg instruction
- __invlpg intrinsic
ms.assetid: 3fb3633f-d9b7-4ec0-9e7f-a7f2fa8ed794
ms.openlocfilehash: 16d8f51c8bf36ea94be7b1325ee5bed256c29693
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97167907"
---
# <a name="__invlpg"></a>__invlpg

**Блок, относящийся только к системам Microsoft**

Создает `invlpg` инструкцию x86, которая делает недействительным БУФЕР TLB преобразования для страницы, связанной с памятью, на которую указывает *адрес*.

## <a name="syntax"></a>Синтаксис

```C
void __invlpg(
   void* Address
);
```

### <a name="parameters"></a>Параметры

*Address*\
окне 64-разрядный адрес.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__invlpg`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Внутренняя функция `__invlpg` создает привилегированную инструкцию и доступна только в режиме ядра с уровнем привилегий (CPL), равным 0.

Эта процедура доступна только как встроенная функция.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
