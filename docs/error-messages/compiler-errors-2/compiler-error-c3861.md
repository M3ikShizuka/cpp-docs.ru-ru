---
description: 'Дополнительные сведения о: Ошибка компилятора C3861'
title: Ошибка компилятора C3861
ms.date: 03/23/2018
f1_keywords:
- C3861
helpviewer_keywords:
- C3861
ms.assetid: 0a1eee30-b3db-41b1-b1e5-35949c3924d7
ms.openlocfilehash: bba259496de09e86b59f9cad1ac1bf89a697a1da
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97222909"
---
# <a name="compiler-error-c3861"></a>Ошибка компилятора C3861

> "*идентификатор*": идентификатор не найден

Компилятору не удалось разрешить ссылку на идентификатор даже при поиске с зависимостью от аргументов.

## <a name="remarks"></a>Комментарии

Чтобы устранить эту ошибку, сравните использование *идентификатора* с объявлением идентификатора для Регистра и проверки орфографии. Убедитесь, что [операторы разрешения области](../../cpp/scope-resolution-operator.md) и пространство имен, [использующие директивы](../../cpp/namespaces-cpp.md#using_directives) , используются правильно. Если идентификатор объявлен в файле заголовка, убедитесь, что заголовок включен перед ссылкой на идентификатор. Если идентификатор должен быть видимым извне, убедитесь, что он объявлен в любом исходном файле, который его использует. Также убедитесь, что объявление идентификатора или определение не исключены [директивами условной компиляции](../../preprocessor/hash-if-hash-elif-hash-else-and-hash-endif-directives-c-cpp.md).

Изменения в удалении устаревших функций из библиотеки времени выполнения C в Visual Studio 2015 могут вызвать C3861. Чтобы устранить эту ошибку, удалите ссылки на эти функции или замените их безопасными альтернативами, если они есть. Дополнительные сведения см. в разделе [устаревшие функции](../../c-runtime-library/obsolete-functions.md).

Если ошибка C3861 появляется после миграции проекта с предыдущих версий компилятора, могут возникнуть проблемы, связанные с поддерживаемыми версиями Windows. Visual C++ больше не поддерживает создание программ для Windows 95, Windows 98, Windows ME, Windows NT и Windows 2000. Если ваши макросы **WINVER** или **_WIN32_WINNT** предназначены для одной из этих версий Windows, необходимо изменить такие макросы. Дополнительные сведения см. в разделе [изменение winver и _WIN32_WINNT](../../porting/modifying-winver-and-win32-winnt.md).

## <a name="examples"></a>Примеры

### <a name="undefined-identifier"></a>Неопределенный идентификатор

Следующий пример приводит к возникновению ошибки C3861, поскольку идентификатор не определен.

```cpp
// C3861.cpp
void f2(){}
int main() {
   f();    // C3861
   f2();   // OK
}
```

### <a name="identifier-not-in-scope"></a>Идентификатор не находится в области

Следующий пример приводит к возникновению ошибки C3861, поскольку идентификатор виден только в области файла его определения, если только он не объявлен в других исходных файлах, которые его используют.

```cpp
// C3861_a1.cpp
// Compile with: cl /EHsc /W4 C3861_a1.cpp C3861_a2.cpp
#include <iostream>
// Uncomment the following line to fix:
// int f();  // declaration makes external function visible
int main() {
   std::cout << f() << std::endl;    // C3861
}
```

```cpp
// C3861_a2.cpp
int f() {  // declared and defined here
   return 42;
}
```

### <a name="namespace-qualification-required"></a>Требуется квалификация пространства имен

Для классов исключений в стандартной библиотеке C++ требуется `std` пространство имен.

```cpp
// C3861_b.cpp
// compile with: /EHsc
#include <iostream>
int main() {
   try {
      throw exception("Exception");   // C3861
      // try the following line instead
      // throw std::exception("Exception");
   }
   catch (...) {
      std::cout << "caught an exception" << std::endl;
   }
}
```

### <a name="obsolete-function-called"></a>Вызвана устаревшая функция

Устаревшие функции были удалены из библиотеки CRT.

```cpp
// C3861_c.cpp
#include <stdio.h>
int main() {
   char line[21]; // room for 20 chars + '\0'
   gets( line );  // C3861
   // Use gets_s instead.
   printf( "The line entered was: %s\n", line );
}
```

### <a name="adl-and-friend-functions"></a>Функции ADL и Friend

Следующий пример приводит к возникновению ошибки C3767, так как компилятор не может использовать поиск с зависимостью от аргумента для `FriendFunc` :

```cpp
namespace N {
   class C {
      friend void FriendFunc() {}
      friend void AnotherFriendFunc(C* c) {}
   };
}

int main() {
   using namespace N;
   FriendFunc();   // C3861 error
   C* pC = new C();
   AnotherFriendFunc(pC);   // found via argument-dependent lookup
}
```

Чтобы устранить эту ошибку, объявите дружественную команду в области класса и определите ее в области видимости пространства имен:

```cpp
class MyClass {
   int m_private;
   friend void func();
};

void func() {
   MyClass s;
   s.m_private = 0;
}

int main() {
   func();
}
```
