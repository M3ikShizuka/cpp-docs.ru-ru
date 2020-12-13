---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4217'
title: Предупреждение средств компоновщика LNK4217
ms.date: 07/23/2019
f1_keywords:
- LNK4217
helpviewer_keywords:
- LNK4217
ms.assetid: 280dc03e-5933-4e8d-bb8c-891fbe788738
ms.openlocfilehash: d3ace3586cf11da4dd87f00a58543c6d60fc1a10
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97150596"
---
# <a name="linker-tools-warning-lnk4217"></a>Предупреждение средств компоновщика LNK4217

> символ "*symbol*", определенный в "*filename_1. obj*", импортируется "*filename_2. obj*" в функции "*Function*"

для символа был указан [__declspec (dllimport)](../../cpp/dllexport-dllimport.md) , хотя символ определен в объектном файле в том же образе. `__declspec(dllimport)`Чтобы устранить это предупреждение, удалите модификатор.

## <a name="remarks"></a>Комментарии

*symbol* — это имя символа, определенное в изображении. *функция* — это функция, которая импортирует символ.

Это предупреждение не появляется при компиляции с параметром [/CLR](../../build/reference/clr-common-language-runtime-compilation.md) .

LNK4217 также может возникнуть при попытке связать два модуля вместе, когда вместо этого следует компилировать второй модуль с помощью библиотеки импорта первого модуля.

```cpp
// main.cpp
__declspec(dllimport) void func();

int main()
{
    func();
    return 0;
}

```

Затем:

```cpp
// tt.cpp
// compile with: /c
void func() {}
```

Попытка скомпилировать эти два модуля, как показано ниже, приведет к LNK4217:

```cmd
cl.exe /c main.cpp tt.cpp
link.exe main.obj tt.obj
```

Чтобы устранить эту ошибку, после компиляции двух файлов передайте TT. obj в lib.exe, чтобы создать LIB-файл, а затем свяжите Main. obj с TT. lib, как показано ниже:

```cmd
cl.exe /c main.cpp tt.cpp
lib.exe tt.obj /export:func /def
link.exe main.obj tt.lib
```

## <a name="see-also"></a>См. также раздел

[Предупреждение средств компоновщика LNK4049](linker-tools-warning-lnk4049.md) \
[Предупреждение средств компоновщика LNK4286](linker-tools-warning-lnk4286.md) \
[dllexport, dllimport](../../cpp/dllexport-dllimport.md)
