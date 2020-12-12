---
description: 'Дополнительные сведения: __outdword'
title: __outdword
ms.date: 09/02/2019
f1_keywords:
- __outdword
helpviewer_keywords:
- out instruction
- outdword instruction
- __outdword intrinsic
ms.assetid: ed1e4994-a84b-4759-8bf9-cd48fb073f4d
ms.openlocfilehash: e1d5f79231675ca64a340138ebda24a56e485ab1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97222350"
---
# <a name="__outdword"></a>__outdword

**Блок, относящийся только к системам Microsoft**

Создает `out` инструкцию для отправки Даублеворд *данных* через *порт* порта.

## <a name="syntax"></a>Синтаксис

```C
void __outdword(
   unsigned short Port,
   unsigned long Data
);
```

### <a name="parameters"></a>Параметры

*Порту*\
окне Порт, в который отправляются данные.

*Данные*\
окне Даублеворд для отправки.

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__outdword`|x86, x64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Эта процедура доступна только как встроенная функция.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
