---
description: 'Дополнительные сведения о: Конвертбстртостринг'
title: ConvertBSTRToString
ms.date: 11/04/2016
f1_keywords:
- ConvertBSTRToString
helpviewer_keywords:
- ConvertBSTRToString function
ms.assetid: ab6ce555-3d75-4e9c-9cb8-ada6d8ce43b1
ms.openlocfilehash: 72d6033003f186f358d9b4143498df65858ee354
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97344618"
---
# <a name="convertbstrtostring"></a>ConvertBSTRToString

**Блок, относящийся только к системам Microsoft**

Преобразует значение типа `BSTR` в значение типа `char *`.

## <a name="syntax"></a>Синтаксис

```
char* __stdcall ConvertBSTRToString(BSTR pSrc);
```

#### <a name="parameters"></a>Параметры

*pSrc*<br/>
Переменная BSTR.

## <a name="remarks"></a>Комментарии

**Конвертбстртостринг** выделяет строку, которую необходимо удалить.

## <a name="example"></a>Пример

```cpp
// ConvertBSTRToString.cpp
#include <comutil.h>
#include <stdio.h>

#pragma comment(lib, "comsuppw.lib")

int main() {
   BSTR bstrText = ::SysAllocString(L"Test");
   wprintf_s(L"BSTR text: %s\n", bstrText);

   char* lpszText2 = _com_util::ConvertBSTRToString(bstrText);
   printf_s("char * text: %s\n", lpszText2);

   SysFreeString(bstrText);
   delete[] lpszText2;
}
```

```Output
BSTR text: Test
char * text: Test
```

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="requirements"></a>Требования

**Заголовок:**\<comutil.h>

**Lib:** комсуппв. lib или комсуппвд. lib (Дополнительные сведения см. в разделе [/Zc: wchar_t (wchar_t является собственным типом)](../build/reference/zc-wchar-t-wchar-t-is-native-type.md)

## <a name="see-also"></a>См. также раздел

[Глобальные функции компилятора COM](../cpp/compiler-com-global-functions.md)
