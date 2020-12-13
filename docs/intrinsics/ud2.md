---
description: 'Дополнительные сведения: __ud2'
title: __ud2
ms.date: 09/02/2019
f1_keywords:
- __ud2
helpviewer_keywords:
- UD2 instruction
- __ud2 intrinsic
ms.assetid: 0831cd5a-8b65-402e-bb57-11e1d5d7ffd2
ms.openlocfilehash: 2b5f0b9ffec066baa3eb2fa212dfc7baf3a6cb49
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333671"
---
# <a name="__ud2"></a>__ud2

**Блок, относящийся только к системам Microsoft**

Создает неопределенную инструкцию.

## <a name="syntax"></a>Синтаксис

```C
void __ud2();
```

## <a name="remarks"></a>Remarks

При выполнении неопределенной инструкции процессор создает исключение недопустимого кода операции.

`__ud2`Функция эквивалентна `UD2` инструкции компьютера и доступна только в режиме ядра. Дополнительные сведения см. в документе "Руководство разработчика по архитектуры Intel, том 2. Справочник по набору инструкций" на сайте корпорации [Intel](https://software.intel.com/articles/intel-sdm) .

## <a name="requirements"></a>Требования

|Intrinsic|Архитектура|
|---------------|------------------|
|`__ud2`|x86, x64|

**Файл заголовка** \<intrin.h>

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="example"></a>Пример

В следующем примере выполняется неопределенная инструкция, которая вызывает исключение. Затем обработчик исключений изменяет код возврата с нуля на один.

```cpp
// __ud2_intrinsic.cpp
#include <stdio.h>
#include <intrin.h>
#include <excpt.h>
// compile with /EHa

int main() {

// Initialize the return code to 0.
int ret = 0;

// Attempt to execute an undefined instruction.
  printf("Before __ud2(). Return code = %d.\n", ret);
  __try {
  __ud2();
  }

// Catch any exceptions and set the return code to 1.
  __except(EXCEPTION_EXECUTE_HANDLER){
  printf("  In the exception handler.\n");
  ret = 1;
  }

// Report the value of the return code.
  printf("After __ud2().  Return code = %d.\n", ret);
  return ret;
}
```

```Output
Before __ud2(). Return code = 0.
  In the exception handler.
After __ud2().  Return code = 1.
```

## <a name="see-also"></a>См. также раздел

[Встроенные функции компилятора](../intrinsics/compiler-intrinsics.md)
