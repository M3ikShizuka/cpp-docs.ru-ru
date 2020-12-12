---
description: 'Дополнительные сведения: __writecr8'
title: __writecr8
ms.date: 09/02/2019
f1_keywords:
- _writecr8
helpviewer_keywords:
- _writecr8 intrinsic
ms.assetid: 6f8bd632-dddb-4335-971e-1acee24aa2b9
ms.openlocfilehash: b9c642d92cd5d5cfb861dbff3d159b5c98a1aa5d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331890"
---
# <a name="__writecr8"></a>__writecr8

**Блок, относящийся только к системам Microsoft**

Записывает значение `Data` в регистр CR8.

## <a name="syntax"></a>Синтаксис

```C
void writecr8(
   unsigned __int64 Data
);
```

### <a name="parameters"></a>Параметры

*Данные*\
окне Значение, записываемое в CR8 регистр.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__writecr8`|X64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

`__writecr8`Встроенная функция доступна только в режиме ядра, и подпрограммы доступны только в качестве встроенных.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
