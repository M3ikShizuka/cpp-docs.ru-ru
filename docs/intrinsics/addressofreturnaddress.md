---
description: 'Дополнительные сведения: _AddressOfReturnAddress'
title: _AddressOfReturnAddress
ms.date: 09/02/2019
f1_keywords:
- _AddressOfReturnAddress_cpp
- _AddressOfReturnAddress
helpviewer_keywords:
- _AddressOfReturnAddress intrinsic
- AddressOfReturnAddress intrinsic
ms.assetid: c7e10b8c-445e-4236-a602-e2d90200f70a
ms.openlocfilehash: 1a79ccbe7ddc2865d8225a62cd0d294f0bc66b4a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97331926"
---
# <a name="_addressofreturnaddress"></a>_AddressOfReturnAddress

**Блок, относящийся только к системам Microsoft**

Предоставляет адрес расположения в памяти, в котором содержится обратный адрес текущей функции. Этот адрес не может использоваться для доступа к другим расположениям в памяти (например, аргументы функции).

## <a name="syntax"></a>Синтаксис

```C
void * _AddressOfReturnAddress();
```

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`_AddressOfReturnAddress`|x86, x64, ARM, ARM64|

**Файл заголовка** \<intrin.h>

## <a name="remarks"></a>Комментарии

Если `_AddressOfReturnAddress` используется в программе, скомпилированной с [параметром/CLR](../build/reference/clr-common-language-runtime-compilation.md), то функция, содержащая `_AddressOfReturnAddress` вызов, компилируется как собственная функция. Если функция, скомпилированная как управляемые вызовы в функцию `_AddressOfReturnAddress` , содержащую, `_AddressOfReturnAddress` может работать не так, как ожидалось.

Эта процедура доступна только как встроенная функция.

## <a name="example"></a>Пример

```cpp
// compiler_intrinsics_AddressOfReturnAddress.cpp
// processor: x86, x64
#include <stdio.h>
#include <intrin.h>

// This function will print three values:
//   (1) The address retrieved from _AddressOfReturnAdress
//   (2) The return address stored at the location returned in (1)
//   (3) The return address retrieved the _ReturnAddress* intrinsic
// Note that (2) and (3) should be the same address.
__declspec(noinline)
void func() {
   void* pvAddressOfReturnAddress = _AddressOfReturnAddress();
   printf_s("%p\n", pvAddressOfReturnAddress);
   printf_s("%p\n", *((void**) pvAddressOfReturnAddress));
   printf_s("%p\n", _ReturnAddress());
}

int main() {
   func();
}
```

```Output
0012FF78
00401058
00401058
```

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)\
[Ключевые слова](../cpp/keywords-cpp.md)
