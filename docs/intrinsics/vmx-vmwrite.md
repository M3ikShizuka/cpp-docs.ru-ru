---
description: 'Дополнительные сведения: __vmx_vmwrite'
title: __vmx_vmwrite
ms.date: 09/02/2019
f1_keywords:
- __vmx_vmwrite
helpviewer_keywords:
- __vmx_vmwrite intrinsic
- VMWRITE instruction
ms.assetid: 88139792-fd3f-4210-97ca-9d84f43a0252
ms.openlocfilehash: d8902d51b05fa96faf22cbb6d80400e1f67c5f3e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97257307"
---
# <a name="__vmx_vmwrite"></a>__vmx_vmwrite

**Блок, относящийся только к системам Microsoft**

Записывает указанное значение в указанное поле в структуре управления текущей виртуальной машиной (VMCS).

## <a name="syntax"></a>Синтаксис

```C
unsigned char __vmx_vmwrite(
   size_t Field,
   size_t FieldValue
);
```

### <a name="parameters"></a>Параметры

*Полями*\
окне Поле VMCS для записи.

*FieldValue*\
окне Значение, записываемое в поле VMCS.

## <a name="return-value"></a>Возвращаемое значение

0,0
Операция успешно выполнена.

одного
Не удалось выполнить операцию; расширенные сведения о состоянии доступны в `VM-instruction error field` текущей структуре VMCS.

открыт
Сбой операции без сведений о состоянии.

## <a name="remarks"></a>Комментарии

Функция `__vmx_vmwrite` эквивалентна инструкции компьютера `VMWRITE` . Значением `Field` параметра является индекс поля в кодировке, описанный в документации Intel. Для получения дополнительной информации выполните поиск приложения C из раздела "Техническая спецификация виртуализации Intel для архитектуры IA-32" на сайте корпорации [Intel](https://software.intel.com/articles/intel-sdm) .

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__vmx_vmwrite`|X64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__vmx_vmread](../intrinsics/vmx-vmread.md)
