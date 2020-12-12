---
description: 'Подробнее о: двойное преобразователь (C++)'
title: Двойное преобразование (С++)
ms.date: 11/04/2016
helpviewer_keywords:
- double thunks
- interop [C++], double thunking
- mixed assemblies [C++], double thunking
- /clr compiler option [C++], double thunking
- interoperability [C++], double thunking
ms.assetid: a85090b2-dc3c-498a-b40c-340db229dd6f
ms.openlocfilehash: 7c09e60ce534dd10567b93ece0eb6cb4bf8cc24a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97252185"
---
# <a name="double-thunking-c"></a>Двойное преобразование (С++)

Двойное перечисление относится к снижению производительности, которое может возникать, когда вызов функции в управляемом контексте вызывает управляемую функцию Visual C++ и когда выполнение программы вызывает собственную точку входа функции для вызова управляемой функции. В этом разделе описывается, где происходит двойное преобразователь и как можно избежать его для повышения производительности.

## <a name="remarks"></a>Комментарии

По умолчанию при компиляции с **параметром/CLR** определение управляемой функции приводит к тому, что компилятор создает управляемую точку входа и собственную точку входа. Это позволяет вызывать управляемую функцию из машинных и управляемых вызовов. Однако при наличии собственной точки входа она может быть точкой входа для всех вызовов функции. Если вызывающая функция является управляемой, собственная точка входа будет вызывать управляемую точку входа. Фактически, для вызова функции требуются два вызова (следовательно, двойное преобразователь). Например, виртуальные функции всегда вызываются с помощью собственной точки входа.

Одним из способов решения этой проблемы является указание компилятору не создавать собственную точку входа для управляемой функции, которую функция будет вызывать только из управляемого контекста с помощью соглашения о вызове [__clrcall](../cpp/clrcall.md) .

Аналогично, если экспортировать ([dllexport, dllimport](../cpp/dllexport-dllimport.md)) управляемую функцию, создается собственная точка входа, а любая функция, которая импортирует и вызывает эту функцию, будет вызываться через собственную точку входа. Чтобы избежать двойного преобразования в этой ситуации, не используйте семантику экспорта и импорта. просто сослаться на метаданные через `#using` (см. [директиву #using](../preprocessor/hash-using-directive-cpp.md)).

Компилятор был обновлен, чтобы сократить ненужный двойной преобразователь. Например, любая функция с управляемым типом в сигнатуре (включая возвращаемый тип) будет неявно помечена как `__clrcall` .

## <a name="example-double-thunking"></a>Пример. двойной преобразователь

### <a name="description"></a>Описание

В следующем примере демонстрируется двойное преобразователь. При компиляции машинного кода (без **/CLR**) вызов виртуальной функции в `main` создает один вызов `T` конструктора копий и один вызов деструктора. Аналогичное поведение достигается при объявлении виртуальной функции с **параметрами/CLR** и `__clrcall` . Однако при компиляции с **параметром/CLR** вызов функции создает вызов конструктора копии, но вызывается еще один вызов конструктора копирования из-за преобразования из машинного в управляемый.

### <a name="code"></a>Код

```cpp
// double_thunking.cpp
// compile with: /clr
#include <stdio.h>
struct T {
   T() {
      puts(__FUNCSIG__);
   }

   T(const T&) {
      puts(__FUNCSIG__);
   }

   ~T() {
      puts(__FUNCSIG__);
   }

   T& operator=(const T&) {
      puts(__FUNCSIG__);
      return *this;
   }
};

struct S {
   virtual void /* __clrcall */ f(T t) {};
} s;

int main() {
   S* pS = &s;
   T t;

   printf("calling struct S\n");
   pS->f(t);
   printf("after calling struct S\n");
}
```

### <a name="sample-output"></a>Пример выходных данных

```
__thiscall T::T(void)
calling struct S
__thiscall T::T(const struct T &)
__thiscall T::T(const struct T &)
__thiscall T::~T(void)
__thiscall T::~T(void)
after calling struct S
__thiscall T::~T(void)
```

## <a name="example-effect-of-double-thunking"></a>Пример. результат двойного преобразования

### <a name="description"></a>Описание

В предыдущем примере продемонстрировано существование двойного преобразователя. Этот пример показывает его результат. **`for`** Цикл вызывает виртуальную функцию, и программа сообщает время выполнения. При компиляции программы с **параметром/CLR** отображается самое медленное время. Когда компиляция выполняется без **параметра/clr** или если виртуальная функция объявлена с `__clrcall` .

### <a name="code"></a>Код

```cpp
// double_thunking_2.cpp
// compile with: /clr
#include <time.h>
#include <stdio.h>

#pragma unmanaged
struct T {
   T() {}
   T(const T&) {}
   ~T() {}
   T& operator=(const T&) { return *this; }
};

struct S {
   virtual void /* __clrcall */ f(T t) {};
} s;

int main() {
   S* pS = &s;
   T t;
   clock_t start, finish;
   double  duration;
   start = clock();

   for ( int i = 0 ; i < 1000000 ; i++ )
      pS->f(t);

   finish = clock();
   duration = (double)(finish - start) / (CLOCKS_PER_SEC);
   printf( "%2.1f seconds\n", duration );
   printf("after calling struct S\n");
}
```

### <a name="sample-output"></a>Пример выходных данных

```
4.2 seconds
after calling struct S
```

## <a name="see-also"></a>См. также раздел

[Смешанные (собственные и управляемые) сборки](../dotnet/mixed-native-and-managed-assemblies.md)
