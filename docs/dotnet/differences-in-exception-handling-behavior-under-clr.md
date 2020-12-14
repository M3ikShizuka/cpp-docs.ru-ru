---
description: Дополнительные сведения о различиях в поведении обработки исключений в параметре/CLR
title: Различия в поведении обработки исключений в среде — CLR
ms.date: 11/04/2016
helpviewer_keywords:
- EXCEPTION_CONTINUE_EXECUTION macro
- set_se_translator function
ms.assetid: 2e7e8daf-d019-44b0-a51c-62d7aaa89104
ms.openlocfilehash: e7e07778e894448fea3d29acb3a32d71884be57c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97252198"
---
# <a name="differences-in-exception-handling-behavior-under-clr"></a>Различия в поведении при обработке исключений в /CLR

[Основные понятия, связанные с использованием управляемых исключений](../dotnet/basic-concepts-in-using-managed-exceptions.md) , обсуждают обработку исключений в управляемых приложениях. В этом разделе подробно рассматриваются отличия стандартного поведения обработки исключений и некоторых ограничений. Дополнительные сведения см. в описании [функции _set_se_translator](../c-runtime-library/reference/set-se-translator.md).

## <a name="jumping-out-of-a-finally-block"></a><a name="vcconjumpingoutofafinallyblock"></a> Выход из блока finally

В машинном коде C/C++ выход из блока __ **finally** с использованием структурированной обработки исключений (SEH) разрешен, хотя выдается предупреждение.  В [параметре/CLR](../build/reference/clr-common-language-runtime-compilation.md)выход из блока **finally** приводит к ошибке:

```cpp
// clr_exception_handling_4.cpp
// compile with: /clr
int main() {
   try {}
   finally {
      return 0;   // also fails with goto, break, continue
    }
}   // C3276
```

## <a name="raising-exceptions-within-an-exception-filter"></a><a name="vcconraisingexceptionswithinanexceptionfilter"></a> Создание исключений в фильтре исключений

При возникновении исключения во время обработки [фильтра исключений](../cpp/writing-an-exception-filter.md) в управляемом коде исключение перехватывается и обрабатывается, как если бы фильтр возвращал значение 0.

Это отличается от поведения в машинном коде, где создается вложенное исключение, поле **ексцептионрекорд** в структуре **EXCEPTION_RECORD** (как возвращено [жетексцептионинформатион](/windows/win32/Debug/getexceptioninformation)), а в поле **ексцептионфлагс** устанавливается бит 0x10. В следующем примере показано различие в поведении:

```cpp
// clr_exception_handling_5.cpp
#include <windows.h>
#include <stdio.h>
#include <assert.h>

#ifndef false
#define false 0
#endif

int *p;

int filter(PEXCEPTION_POINTERS ExceptionPointers) {
   PEXCEPTION_RECORD ExceptionRecord =
                     ExceptionPointers->ExceptionRecord;

   if ((ExceptionRecord->ExceptionFlags & 0x10) == 0) {
      // not a nested exception, throw one
      *p = 0; // throw another AV
   }
   else {
      printf("Caught a nested exception\n");
      return 1;
    }

   assert(false);

   return 0;
}

void f(void) {
   __try {
      *p = 0;   // throw an AV
   }
   __except(filter(GetExceptionInformation())) {
      printf_s("We should execute this handler if "
                 "compiled to native\n");
    }
}

int main() {
   __try {
      f();
   }
   __except(1) {
      printf_s("The handler in main caught the "
               "exception\n");
    }
}
```

### <a name="output"></a>Выходные данные

```Output
Caught a nested exception
We should execute this handler if compiled to native
```

## <a name="disassociated-rethrows"></a><a name="vccondisassociatedrethrows"></a> Несвязанные повторные выдачи

**параметр/CLR** не поддерживает повторный вызов исключения за пределами обработчика catch (называемого несвязанным повторным вызовом). Исключения этого типа рассматриваются как стандартный повторный вызов C++. Если обнаружено несвязанное повторное исключение при наличии активного управляемого исключения, исключение упаковывается как исключение C++, а затем вызывается повторно. Исключения этого типа могут быть перехвачены только как исключение типа <xref:System.Runtime.InteropServices.SEHException> .

В следующем примере показано повторное возникновение управляемого исключения в виде исключения C++:

```cpp
// clr_exception_handling_6.cpp
// compile with: /clr
using namespace System;
#include <assert.h>
#include <stdio.h>

void rethrow( void ) {
   // This rethrow is a dissasociated rethrow.
   // The exception would be masked as SEHException.
   throw;
}

int main() {
   try {
      try {
         throw gcnew ApplicationException;
      }
      catch ( ApplicationException^ ) {
         rethrow();
         // If the call to rethrow() is replaced with
         // a throw statement within the catch handler,
         // the rethrow would be a managed rethrow and
         // the exception type would remain
         // System::ApplicationException
      }
   }

    catch ( ApplicationException^ ) {
      assert( false );

      // This will not be executed since the exception
      // will be masked as SEHException.
    }
   catch ( Runtime::InteropServices::SEHException^ ) {
      printf_s("caught an SEH Exception\n" );
    }
}
```

### <a name="output"></a>Выходные данные

```Output
caught an SEH Exception
```

## <a name="exception-filters-and-exception_continue_execution"></a><a name="vcconexceptionfiltersandexception_continue_execution"></a> Фильтры исключений и EXCEPTION_CONTINUE_EXECUTION

Если фильтр возвращается `EXCEPTION_CONTINUE_EXECUTION` в управляемом приложении, он обрабатывается так, как если бы был возвращен фильтр `EXCEPTION_CONTINUE_SEARCH` . Дополнительные сведения об этих константах см. в разделе [оператор try-except](../cpp/try-except-statement.md).

Это различие показано в следующем примере:

```cpp
// clr_exception_handling_7.cpp
#include <windows.h>
#include <stdio.h>
#include <assert.h>

int main() {
   int Counter = 0;
   __try {
      __try  {
         Counter -= 1;
         RaiseException (0xe0000000|'seh',
                         0, 0, 0);
         Counter -= 2;
      }
      __except (Counter) {
         // Counter is negative,
         // indicating "CONTINUE EXECUTE"
         Counter -= 1;
      }
    }
    __except(1) {
      Counter -= 100;
   }

   printf_s("Counter=%d\n", Counter);
}
```

### <a name="output"></a>Выходные данные

```Output
Counter=-3
```

## <a name="the-_set_se_translator-function"></a><a name="vcconthe_set_se_translatorfunction"></a> Функция _set_se_translator

Функция-переводчик, заданная путем вызова функции `_set_se_translator` , влияет только на перехваты в неуправляемом коде. Это ограничение показано в следующем примере:

```cpp
// clr_exception_handling_8.cpp
// compile with: /clr /EHa
#include <iostream>
#include <windows.h>
#include <eh.h>
#pragma warning (disable: 4101)
using namespace std;
using namespace System;

#define MYEXCEPTION_CODE 0xe0000101

class CMyException {
public:
   unsigned int m_ErrorCode;
   EXCEPTION_POINTERS * m_pExp;

   CMyException() : m_ErrorCode( 0 ), m_pExp( NULL ) {}

   CMyException( unsigned int i, EXCEPTION_POINTERS * pExp )
         : m_ErrorCode( i ), m_pExp( pExp ) {}

   CMyException( CMyException& c ) : m_ErrorCode( c.m_ErrorCode ),
                                      m_pExp( c.m_pExp ) {}

   friend ostream& operator <<
                 ( ostream& out, const CMyException& inst ) {
      return out <<  "CMyException[\n" <<
             "Error Code: " << inst.m_ErrorCode <<  "]";
    }
};

#pragma unmanaged
void my_trans_func( unsigned int u, PEXCEPTION_POINTERS pExp ) {
   cout <<  "In my_trans_func.\n";
   throw CMyException( u, pExp );
}

#pragma managed
void managed_func() {
   try  {
      RaiseException( MYEXCEPTION_CODE, 0, 0, 0 );
   }
   catch ( CMyException x ) {}
   catch ( ... ) {
      printf_s("This is invoked since "
               "_set_se_translator is not "
               "supported when /clr is used\n" );
    }
}

#pragma unmanaged
void unmanaged_func() {
   try  {
      RaiseException( MYEXCEPTION_CODE,
                      0, 0, 0 );
   }
   catch ( CMyException x ) {
      printf("Caught an SEH exception with "
             "exception code: %x\n", x.m_ErrorCode );
    }
    catch ( ... ) {}
}

// #pragma managed
int main( int argc, char ** argv ) {
   _set_se_translator( my_trans_func );

   // It does not matter whether the translator function
   // is registered in managed or unmanaged code
   managed_func();
   unmanaged_func();
}
```

### <a name="output"></a>Вывод

```Output
This is invoked since _set_se_translator is not supported when /clr is used
In my_trans_func.
Caught an SEH exception with exception code: e0000101
```

## <a name="see-also"></a>См. также

[Обработка исключений](../extensions/exception-handling-cpp-component-extensions.md)<br/>
[safe_cast](../extensions/safe-cast-cpp-component-extensions.md)<br/>
[Обработка исключений в КОМПИЛЯТОРОМ MSVC](../cpp/exception-handling-in-visual-cpp.md)
