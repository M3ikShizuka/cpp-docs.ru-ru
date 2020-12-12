---
description: 'Подробнее: Общие сведения о маршалировании в C++/CLI'
title: Общие сведения о маршалировании в C++
ms.date: 07/12/2019
ms.topic: reference
f1_keywords:
- marshaling
- marshalling
helpviewer_keywords:
- Visual C++, marshaling
- C++ Support Library, marshaling
- marshaling, about marshaling
ms.assetid: 997dd4bc-5f98-408f-b890-f35de9ce3bb8
ms.openlocfilehash: 35294a204d338087a609746e6ae2e5e07ea07b59
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97255539"
---
# <a name="overview-of-marshaling-in-ccli"></a>Общие сведения о маршалировании в C++/CLI

В смешанном режиме иногда требуется маршалировать данные между собственными и управляемыми типами. *Библиотека упаковки* упрощает маршалирование и преобразование данных простым способом.  Библиотека упаковки состоит из набора функций и `marshal_context` класса, выполняющего маршалирование для общих типов. Библиотека определена в этих заголовках каталога **include/мсклр** для вашего выпуска Visual Studio:

|Header|Описание|
|---------------|-----------------|
|Marshal. h|`marshal_context` классы и контекстно-ориентированные функции упаковки|
|marshal_atl. h| Функции для маршалирования типов ATL|
|marshal_cppstd. h|Функции для маршалирования стандартных типов C++|
|marshal_windows. h|Функции для маршалирования типов окон|

Путь по умолчанию для папки **мсклр** выглядит примерно так, как в зависимости от имеющегося выпуска и номера сборки:

```cmd
C:\\Program Files (x86)\\Microsoft Visual Studio\\Preview\\Enterprise\\VC\\Tools\\MSVC\\14.15.26528\\include\\msclr
```

Библиотеку можно использовать с [классом marshal_context](../dotnet/marshal-context-class.md)или без него. Для некоторых преобразований требуется контекст. Другие преобразования можно реализовать с помощью функции [marshal_as](../dotnet/marshal-as.md) . В следующей таблице перечислены поддерживаемые преобразования, указаны ли они в контексте и какой файл маршалирования необходимо включить.

|Из типа|В тип|Метод Marshal|Включаемый файл|
|---------------|-------------|--------------------|------------------|
|System:: строка ^|const char \*|marshal_context|Marshal. h|
|const char \*|System:: строка ^|marshal_as|Marshal. h|
|типа \*|System:: строка ^|marshal_as|Marshal. h|
|System:: строка ^|константное wchar_t\*|marshal_context|Marshal. h|
|константное wchar_t \*|System:: строка ^|marshal_as|Marshal. h|
|wchar_t \*|System:: строка ^|marshal_as|Marshal. h|
|System:: IntPtr|HANDLE|marshal_as|marshal_windows. h|
|HANDLE|System:: IntPtr|marshal_as|marshal_windows. h|
|System:: строка ^|BSTR|marshal_context|marshal_windows. h|
|BSTR|System:: строка ^|marshal_as|Marshal. h|
|System:: строка ^|bstr_t|marshal_as|marshal_windows. h|
|bstr_t|System:: строка ^|marshal_as|marshal_windows. h|
|System:: строка ^|std:: String|marshal_as|marshal_cppstd. h|
|std:: String|System:: строка ^|marshal_as|marshal_cppstd. h|
|System:: строка ^|std::wstring|marshal_as|marshal_cppstd. h|
|std::wstring|System:: строка ^|marshal_as|marshal_cppstd. h|
|System:: строка ^|CStringT\<char>|marshal_as|marshal_atl. h|
|CStringT\<char>|System:: строка ^|marshal_as|marshal_atl. h|
|System:: строка ^|CStringT<wchar_t>|marshal_as|marshal_atl. h|
|CStringT<wchar_t>|System:: строка ^|marshal_as|marshal_atl. h|
|System:: строка ^|CComBSTR|marshal_as|marshal_atl. h|
|CComBSTR|System:: строка ^|marshal_as|marshal_atl. h|

Для маршалирования требуется контекст только при маршалировании из управляемых типов данных, а собственный тип, в котором выполняется преобразование, не имеет деструктора для автоматической очистки. Контекст маршалирования уничтожает выделенный собственный тип данных в его деструкторе. Поэтому преобразования, требующие контекста, будут действительны только до тех пор, пока не будет удален контекст. Чтобы сохранить все упакованные значения, необходимо скопировать значения в собственные переменные.

> [!NOTE]
> Если в строке есть внедренные `NULL` элементы, результат маршалирования строки не гарантируется. Внедренный элемент `NULL` s может привести к усечению строки или сохранить их.

В этом примере показано, как включить каталог мсклр в объявление заголовка include:

`#include "msclr\marshal_cppstd.h"`

Библиотека упаковки расширяема, поэтому можно добавлять собственные типы маршалирования. Дополнительные сведения о расширении библиотеки для маршалирования см. в разделе [как расширить библиотеку маршалирования](../dotnet/how-to-extend-the-marshaling-library.md).

## <a name="see-also"></a>См. также раздел

[Библиотека поддержки C++](../dotnet/cpp-support-library.md)<br/>
[Руководство. расширение библиотеки для маршалирования](../dotnet/how-to-extend-the-marshaling-library.md)
