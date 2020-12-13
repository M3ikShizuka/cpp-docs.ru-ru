---
description: 'Дополнительные сведения: __writegsbyte, __writegsdword, __writegsqword, __writegsword'
title: __writegsbyte, __writegsdword, __writegsqword, __writegsword
ms.date: 09/02/2019
f1_keywords:
- __writegsbyte
- __writegsqword
- __writegsdword
- __writegsword
helpviewer_keywords:
- __writegsqword intrinsic
- __writegsbyte intrinsic
- __writegsword intrinsic
- __writegsdword intrinsic
ms.assetid: 7746cf6d-2259-4139-9aab-c07dd75c8037
ms.openlocfilehash: e3dd3284d38f4c1518fbf5f7184d15fc0c9d67d0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331834"
---
# <a name="__writegsbyte-__writegsdword-__writegsqword-__writegsword"></a>__writegsbyte, __writegsdword, __writegsqword, __writegsword

**Блок, относящийся только к системам Microsoft**

Запись памяти в расположение, заданное смещением относительно начала сегмента GS.

## <a name="syntax"></a>Синтаксис

```C
void __writegsbyte(
   unsigned long Offset,
   unsigned char Data
);
void __writegsword(
   unsigned long Offset,
   unsigned short Data
);
void __writegsdword(
   unsigned long Offset,
   unsigned long Data
);
void __writegsqword(
   unsigned long Offset,
   unsigned __int64 Data
);
```

### <a name="parameters"></a>Параметры

*Собой*\
окне Смещение от начала GS для записи.

*Данные*\
окне Записываемое значение.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__writegsbyte`|X64|
|`__writegsdword`|X64|
|`__writegsqword`|X64|
|`__writegsword`|X64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эти подпрограммы доступны только в качестве встроенных.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[__readgsbyte, \_ _readgsdword, \_ _readgsqword, \_ _readgsword](../intrinsics/readgsbyte-readgsdword-readgsqword-readgsword.md)\
[Встроенные объекты компилятора](../intrinsics/compiler-intrinsics.md)
