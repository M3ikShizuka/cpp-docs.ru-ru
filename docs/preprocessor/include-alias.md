---
description: 'Дополнительные сведения о: include_alias pragma'
title: Прагма include_alias
ms.date: 08/29/2019
f1_keywords:
- vc-pragma.include_alias
- include_alias_CPP
helpviewer_keywords:
- pragmas, include_alias
- include_alias pragma
ms.assetid: 3256d589-12b3-4af0-a586-199e96eabacc
ms.openlocfilehash: 1a1855ce4c908c6678cfce7617c98aa671c57fac
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97236520"
---
# <a name="include_alias-pragma"></a>Прагма include_alias

Указывает, что при обнаружении *alias_filename* в `#include` директиве компилятор замещает *actual_filename* на своем месте.

## <a name="syntax"></a>Синтаксис

<!-- localization note - it's important to have the italic and bold characters immediately adjacent here. -->
> **#pragma include_alias (** "*alias_filename*" **,** "*actual_filename*" **)**\
> **include_alias #pragma (** \<*alias_filename*> **,** \<*actual_filename*> **)**

## <a name="remarks"></a>Комментарии

Директива pragma **include_alias** позволяет заменять файлы с разными именами или путями для имен файлов, включаемых в исходные файлы. Например, некоторые файловые системы допускают более длинные имена файлов заголовков, чем ограничение файловой системы FAT 8,3. Компилятор не может просто усечь более длинные имена до 8,3, так как первые восемь символов из длинных имен файлов заголовков могут быть неуникальными. Всякий раз, когда компилятор видит *alias_filenameную* строку в `#include` директиве, вместо нее подставляется имя *actual_filename* . Затем загружается файл заголовка *actual_filename* . Эта директива pragma должна располагаться до соответствующей директивы `#include`. Пример:

```cpp
// First eight characters of these two files not unique.
#pragma include_alias( "AppleSystemHeaderQuickdraw.h", "quickdra.h" )
#pragma include_alias( "AppleSystemHeaderFruit.h", "fruit.h" )

#pragma include_alias( "GraphicsMenu.h", "gramenu.h" )

#include "AppleSystemHeaderQuickdraw.h"
#include "AppleSystemHeaderFruit.h"
#include "GraphicsMenu.h"
```

Псевдоним для поиска должен точно соответствовать спецификации. Регистр, Орфография и использование двойных кавычек или угловых скобок должны совпадать. Директива pragma **include_alias** выполняет простое сопоставление строк по именам файлов. Другие проверки имени файла не выполняются. Рассмотрим директивы в следующем примере:

```cpp
#pragma include_alias("mymath.h", "math.h")
#include "./mymath.h"
#include "sys/mymath.h"
```

Подстановка псевдонимов не выполняется, так как строки файла заголовка не совпадают в точности. Кроме того, имена файлов заголовков, используемые в качестве аргументов для `/Yu` `/Yc` параметров компилятора и, или `hdrstop` директивы pragma, не подставляются. Например, представим, что исходный файл содержит следующую директиву:

```cpp
#include <AppleSystemHeaderStop.h>
```

В этом случае должен использоваться следующий параметр компилятора:

> **/икапплесистемхеадерстоп.х**

С помощью директивы pragma **include_alias** можно сопоставлять любое имя файла заголовка с другим. Пример:

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

Ошибка в *верилонгфиленаме. H* выдает следующее сообщение об ошибке:

```Output
myfile.h(15) : error C2059 : syntax error
```

Также обратите внимание, что транзитивность не поддерживается. Рассмотрим следующий пример:

```cpp
#pragma include_alias( "one.h", "two.h" )
#pragma include_alias( "two.h", "three.h" )
#include "one.h"
```

компилятор ищет файл *2. h* , а не *3. h*.

## <a name="see-also"></a>См. также раздел

[Директивы pragma и ключевое слово __pragma](../preprocessor/pragma-directives-and-the-pragma-keyword.md)
