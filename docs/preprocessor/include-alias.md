---
description: Дополнительные сведения об pragma директиве include_alias в Microsoft C/C++
title: include_alias pragma
ms.date: 01/22/2021
f1_keywords:
- vc-pragma.include_alias
- include_alias_CPP
helpviewer_keywords:
- pragma, include_alias
- include_alias pragma
no-loc:
- pragma
ms.openlocfilehash: a9586748794704b3b3bcaf3d8ede7ef2f2f74545
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713601"
---
# <a name="include_alias-no-locpragma"></a>`include_alias` pragma

Указывает, что при обнаружении *alias_filename* в `#include` директиве компилятор замещает *actual_filename* на своем месте.

## <a name="syntax"></a>Синтаксис

<!-- localization note - it's important to have the italic and bold characters immediately adjacent here. -->
> **`#pragma include_alias(`** "*alias_filename*" **`,`** *actual_filename*" **`)`**\
> **`#pragma include_alias(`** \<*alias_filename*> **`,`** \<*actual_filename*> **`)`**

## <a name="remarks"></a>Примечания

**`include_alias`** pragma Директива позволяет заменять файлы с разными именами или путями для имен файлов, включаемых в исходные файлы. Например, некоторые файловые системы допускают более длинные имена файлов заголовков, чем ограничение файловой системы FAT 8,3. Компилятор не может просто усечь более длинные имена до 8,3, так как первые восемь символов из длинных имен файлов заголовков могут быть неуникальными. Всякий раз, когда компилятор видит *alias_filenameную* строку в `#include` директиве, вместо нее подставляется имя *actual_filename* . Затем загружается файл заголовка *actual_filename* . Он pragma должен располагаться перед соответствующими `#include` директивами. Например:

```cpp
// First eight characters of these two files not unique.
#pragma include_alias( "AppleSystemHeaderQuickdraw.h", "quickdra.h" )
#pragma include_alias( "AppleSystemHeaderFruit.h", "fruit.h" )

#pragma include_alias( "GraphicsMenu.h", "gramenu.h" )

#include "AppleSystemHeaderQuickdraw.h"
#include "AppleSystemHeaderFruit.h"
#include "GraphicsMenu.h"
```

Псевдоним для поиска должен точно соответствовать спецификации. Регистр, Орфография и использование двойных кавычек или угловых скобок должны совпадать. **`include_alias`** pragma Выполняет простое сопоставление строк по именам файлов. Другие проверки имени файла не выполняются. Рассмотрим директивы в следующем примере:

```cpp
#pragma include_alias("mymath.h", "math.h")
#include "./mymath.h"
#include "sys/mymath.h"
```

Подстановка псевдонимов не выполняется, так как строки файла заголовка не совпадают в точности. Кроме того, имена файлов заголовков, используемые в качестве аргументов для **`/Yu`** **`/Yc`** параметров компилятора и, или `hdrstop` pragma , не заменяются. Например, представим, что исходный файл содержит следующую директиву:

```cpp
#include <AppleSystemHeaderStop.h>
```

В этом случае должен использоваться следующий параметр компилятора:

> **`/YcAppleSystemHeaderStop.h`**

С помощью можно **`include_alias`** pragma сопоставлять любое имя файла заголовка с другим. Например:

```cpp
#pragma include_alias( "api.h", "c:\version1.0\api.h" )
#pragma include_alias( <stdio.h>, <newstdio.h> )
#include "api.h"
#include <stdio.h>
```

Не следует смешивать имена файлов, заключенные в двойные кавычки, с именами, заключенными в угловые скобки. Например, при наличии двух вышеупомянутых `#pragma include_alias` директив компилятор не выполняет подстановку для следующих `#include` директив:

```cpp
#include <api.h>
#include "stdio.h"
```

Кроме того, следующая директива вызовет ошибку:

```cpp
#pragma include_alias(<header.h>, "header.h")  // Error
```

Имя файла, сообщаемое в сообщениях об ошибках, или в качестве значения предопределенного `__FILE__` макроса, будет являться именем, заданным после завершения подстановки. Например, см. выходные данные после следующих директив:

```cpp
#pragma include_alias( "VERYLONGFILENAME.H", "myfile.h" )
#include "VERYLONGFILENAME.H"
```

Ошибка в *`VERYLONGFILENAME.H`* выдает следующее сообщение об ошибке:

```Output
myfile.h(15) : error C2059 : syntax error
```

Также обратите внимание, что транзитивность не поддерживается. Рассмотрим следующий пример:

```cpp
#pragma include_alias( "one.h", "two.h" )
#pragma include_alias( "two.h", "three.h" )
#include "one.h"
```

компилятор ищет файл, *`two.h`* а не *`three.h`* .

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
