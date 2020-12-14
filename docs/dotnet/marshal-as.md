---
description: 'Дополнительные сведения: marshal_as'
title: marshal_as
ms.date: 07/12/2019
ms.topic: reference
f1_keywords:
- marshal_as
- msclr.interop.marshal_as
- msclr::interop::marshal_as
helpviewer_keywords:
- marshal_as template [C++]
ms.assetid: 2ed717da-2b11-41e5-981d-47d251771989
ms.openlocfilehash: 0b0738b8778b287e2e97f074345a10841c70a7b1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97253628"
---
# <a name="marshal_as"></a>marshal_as

Этот метод преобразует данные между собственными и управляемыми средами.

## <a name="syntax"></a>Синтаксис

```
To_Type marshal_as<To_Type>(
   From_Type input
);
```

#### <a name="parameters"></a>Параметры

*input*<br/>
окне Значение, которое необходимо маршалировать в `To_Type` переменную.

## <a name="return-value"></a>Возвращаемое значение

Переменная типа `To_Type` , которая является преобразованным значением `input` .

## <a name="remarks"></a>Комментарии

Этот метод является упрощенным способом преобразования данных между собственными и управляемыми типами. Чтобы определить, какие типы данных поддерживаются, см. раздел [Общие сведения о маршалировании в C++](../dotnet/overview-of-marshaling-in-cpp.md). Для некоторых преобразований данных требуется контекст. Эти типы данных можно преобразовать с помощью [класса marshal_context](../dotnet/marshal-context-class.md).

При попытке маршалирования пары типов данных, которые не поддерживаются, `marshal_as` выдает ошибку [C4996](../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md) во время компиляции. Дополнительные сведения см. в сообщении, прилагаемом к этой ошибке. Эта `C4996` ошибка может быть создана для более чем нерекомендуемых функций. Одним из примеров является попытка маршалирования пары типов данных, которые не поддерживаются.

Библиотека упаковки состоит из нескольких файлов заголовков. Для любого преобразования требуется только один файл, но при необходимости для других преобразований можно включить дополнительные файлы. Чтобы узнать, какие преобразования связаны с файлами, просмотрите таблицу в `Marshaling Overview` . Независимо от того, какое преобразование необходимо выполнить, требование к пространству имен всегда действует.

Вызывает, `System::ArgumentNullException(_EXCEPTION_NULLPTR)` Если входной параметр имеет значение null.

## <a name="example"></a>Пример

В этом примере выполняется упаковка из `const char*` типа в `System::String` переменную.

```cpp
// marshal_as_test.cpp
// compile with: /clr
#include <stdlib.h>
#include <string.h>
#include <msclr\marshal.h>

using namespace System;
using namespace msclr::interop;

int main() {
   const char* message = "Test String to Marshal";
   String^ result;
   result = marshal_as<String^>( message );
   return 0;
}
```

## <a name="requirements"></a>Требования

**Заголовочный файл:** \<msclr\marshal.h> , \<msclr\marshal_windows.h> , \<msclr\marshal_cppstd.h> или \<msclr\marshal_atl.h>

**Пространство имен:** мсклр:: Interop

## <a name="see-also"></a>См. также раздел

[Общие сведения о маршалировании в C++](../dotnet/overview-of-marshaling-in-cpp.md)<br/>
[Класс marshal_context](../dotnet/marshal-context-class.md)
