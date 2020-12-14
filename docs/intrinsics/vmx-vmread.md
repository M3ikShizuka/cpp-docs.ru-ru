---
description: 'Дополнительные сведения: __vmx_vmread'
title: __vmx_vmread
ms.date: 09/02/2019
f1_keywords:
- __vmx_vmread
helpviewer_keywords:
- VMREAD instruction
- __vmx_vmread intrinsic
ms.assetid: 08bdd7a0-6435-4ea6-b9a0-f592d870e5aa
ms.openlocfilehash: 39ea9c0566d3f9c9d3fc6d980861fb3580293895
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333514"
---
# <a name="__vmx_vmread"></a>__vmx_vmread

**Блок, относящийся только к системам Microsoft**

Считывает указанное поле из текущей структуры управления виртуальной машины (VMCS) и помещает его в указанное расположение.

## <a name="syntax"></a>Синтаксис

```C
unsigned char __vmx_vmread(
   size_t Field,
   size_t *FieldValue
);
```

### <a name="parameters"></a>Параметры

*Полями*\
окне Поле VMCS для чтения.

*FieldValue*\
окне Указатель на место хранения значения, считанного из поля VMCS, указанного `Field` параметром.

## <a name="return-value"></a>Возвращаемое значение

|Значение|Значение|
|-----------|-------------|
|0|Операция успешно выполнена.|
|1|Не удалось выполнить операцию; расширенные сведения о состоянии доступны в `VM-instruction error field` текущей структуре VMCS.|
|2|Сбой операции без сведений о состоянии.|

## <a name="remarks"></a>Комментарии

Функция `__vmx_vmread` эквивалентна инструкции компьютера `VMREAD` . Значением `Field` параметра является индекс поля в кодировке, описанный в документации Intel. Для получения дополнительной информации выполните поиск приложения C из раздела "Техническая спецификация виртуализации Intel для архитектуры IA-32" на сайте корпорации [Intel](https://software.intel.com/articles/intel-sdm) .

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__vmx_vmread`|X64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[__vmx_vmwrite](../intrinsics/vmx-vmwrite.md)
