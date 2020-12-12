---
description: 'Дополнительные сведения: Передача аргументов CString'
title: Передача аргументов CString
ms.date: 11/04/2016
helpviewer_keywords:
- strings [C++], as function input/output
- argument passing [C++]
- arguments [C++], passing
- functions [C++], strings as input/output
- argument passing [C++], C strings
- passing arguments, C strings
- CString objects, passing arguments
- string arguments
ms.assetid: a67bebff-edf1-4cf4-bbff-d1cc6a901099
ms.openlocfilehash: ee47898ffdfc5129b11b0f9480669fa142d12818
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97167179"
---
# <a name="cstring-argument-passing"></a>Передача аргументов CString

В этой статье объясняется, как передавать объекты [CString](../atl-mfc-shared/reference/cstringt-class.md) в функции и как возвращать `CString` объекты из функций.

## <a name="cstring-argument-passing-conventions"></a><a name="_core_cstring_argument.2d.passing_conventions"></a> Соглашения Argument-Passing CString

При определении интерфейса класса необходимо определить соглашение о передаче аргументов для функций-членов. Существуют стандартные правила передачи и возврата `CString` объектов. Если следовать правилам, описанным в разделе [строки как входные](#_core_strings_as_function_inputs) и [строковые функции в качестве выходных данных функции](#_core_strings_as_function_outputs), вы получите эффективный и правильный код.

## <a name="strings-as-function-inputs"></a><a name="_core_strings_as_function_inputs"></a> Строки как входные данные функции

Самым эффективным и безопасным способом использования `CString` объекта в вызываемых функциях является передача объекта в `CString` функцию. Несмотря на имя, объект не `CString` сохраняет строку внутри как строку в стиле C, имеющую признак конца null. Вместо этого объект следит за тем, чтобы `CString` проследить количество символов в нем. Наличие `CString` указателя LPCTSTR на строку, завершающуюся нулем, является небольшим объемом работы, который может стать значительным, если код должен постоянно выполнять его. Результат является временным, так как любое изменение `CString` содержимого сделает недействительными старые копии указателя LPCTSTR.

В некоторых случаях имеет смысл предоставить строку в стиле C. Например, может возникнуть ситуация, когда вызываемая функция написана на языке C и не поддерживает объекты. В этом случае `CString` применяет параметр к LPCTSTR, и функция получает строку с завершающим нулем в стиле C. Можно также переключиться на другое направление и создать `CString` объект с помощью `CString` конструктора, принимающего строковый параметр в стиле C.

Если содержимое строки должно быть изменено функцией, объявите параметр как неконстантную `CString` ссылку ( `CString&` ).

## <a name="strings-as-function-outputs"></a><a name="_core_strings_as_function_outputs"></a> Строки как выходные данные функции

Обычно можно возвращать `CString` объекты из функций, так как `CString` объекты следуют семантике значений, например типам-примитивам. Чтобы получить доступ к строке только для чтения, используйте константную `CString` ссылку ( `const CString&` ). В следующем примере показано использование `CString` параметров и возвращаемых типов.

[!code-cpp[NVC_ATLMFC_Utilities#197](../atl-mfc-shared/codesnippet/cpp/cstring-argument-passing_1.cpp)]

[!code-cpp[NVC_ATLMFC_Utilities#198](../atl-mfc-shared/codesnippet/cpp/cstring-argument-passing_2.cpp)]

## <a name="see-also"></a>См. также раздел

[Строки (ATL и MFC)](../atl-mfc-shared/strings-atl-mfc.md)
