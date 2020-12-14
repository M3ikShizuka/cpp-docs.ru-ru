---
description: 'Дополнительные сведения о: Ошибка компилятора C2441'
title: Ошибка компилятора C2441
ms.date: 11/04/2016
f1_keywords:
- C2441
helpviewer_keywords:
- C2441
ms.assetid: ffbd6573-777a-48dd-892f-5cf4a758dcab
ms.openlocfilehash: d7a6073be821fcd2717caae258c5b3f397fb3f87
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97189734"
---
# <a name="compiler-error-c2441"></a>Ошибка компилятора C2441

> "*переменная*": символ, объявленный с __declspec (Process), должен быть константой в режиме/clr: pure

## <a name="remarks"></a>Комментарии

Параметры компилятора **/clr: pure** и **/clr: Сейф** являются устаревшими в Visual Studio 2015 и не поддерживаются в Visual Studio 2017.

По умолчанию переменные задаются для каждого домена приложения в **параметре/CLR: pure**. Переменная, помеченная как `__declspec(process)` **/clr: pure** , подвержена ошибкам, если она изменена в одном домене приложения и считывается в другом.

Таким образом, компилятор принудительно применяет переменные для каждого процесса в режиме **`const`** **/clr: pure**, делая их только для чтения во всех доменах приложений.

Дополнительные сведения см. в разделе [Process](../../cpp/process.md) и [/CLR (компиляция общеязыковой среды выполнения)](../../build/reference/clr-common-language-runtime-compilation.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2441.

```cpp
// C2441.cpp
// compile with: /clr:pure /c
__declspec(process) int i;   // C2441
__declspec(process) const int j = 0;   // OK
```
