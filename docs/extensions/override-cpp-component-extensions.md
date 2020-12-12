---
description: 'Дополнительные сведения о: override (C++/CLI и C++/CX)'
title: override (C++/CLI и C++/CX)
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- overriding, override keyword [C++]
- override keyword [C++]
ms.assetid: 34d19257-1686-4fcd-96f5-af07c70ba914
ms.openlocfilehash: 1be49ac9b9e2d0f2eb3342855a42e9707f883078
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335944"
---
# <a name="override--ccli-and-ccx"></a>override (C++/CLI и C++/CX)

Контекстно-зависимое ключевое слово **override** указывает, что член типа переопределяет член базового класса или базового интерфейса.

## <a name="remarks"></a>Комментарии

Ключевое слово **override** обрабатывается при компиляции в машинный код (параметр компилятора по умолчанию), объекты среды выполнения Windows (параметр компиляции `/ZW`) или объекты среды CLR (параметр компилятора `/clr`).

Подробные сведения об описателях переопределения см. в статье [override Specifier](../cpp/override-specifier.md) (Описатель override) и [Override Specifiers and Native Compilations](../dotnet/how-to-declare-override-specifiers-in-native-compilations-cpp-cli.md) (Описатели переопределения и компиляции в машинный код).

Подробные сведения о контекстно-зависимых ключевых словах см. в статье [Context-Sensitive Keywords (C++/CLI and C++/CX)](context-sensitive-keywords-cpp-component-extensions.md) (Контекстно-зависимые ключевые слова (C++/CLI and C++/CX)).

## <a name="examples"></a>Примеры

В следующем примере кода показано, как **override** также можно использовать в компиляциях в машинный код.

```cpp
// override_keyword_1.cpp
// compile with: /c
struct I1 {
   virtual void f();
};

struct X : public I1 {
   virtual void f() override {}
};
```

### <a name="example"></a>Пример

В следующем примере кода показано, как **override** также можно использовать в компиляциях в объекты среды выполнения Windows.

```cpp
// override_keyword_2.cpp
// compile with: /ZW /c
ref struct I1 {
   virtual void f();
};

ref struct X : public I1 {
   virtual void f() override {}
};
```

#### <a name="requirements"></a>Требования

Параметр компилятора: `/ZW`

### <a name="example"></a>Пример

В следующем примере кода показано, как **override** также можно использовать в компиляциях в объекты среды CLR.

```cpp
// override_keyword_3.cpp
// compile with: /clr /c
ref struct I1 {
   virtual void f();
};

ref struct X : public I1 {
   virtual void f() override {}
};
```

#### <a name="requirements"></a>Требования

Параметр компилятора: `/clr`

## <a name="see-also"></a>См. также раздел

[Спецификатор переопределения](../cpp/override-specifier.md)<br/>
[Спецификаторы переопределения](override-specifiers-cpp-component-extensions.md)
