---
description: 'Дополнительные сведения о: __identifier (C++/CLI)'
title: __identifier (C++/CLI)
ms.date: 10/12/2018
ms.topic: reference
f1_keywords:
- __identifier
- __identifier_cpp
helpviewer_keywords:
- __identifier keyword [C++]
ms.assetid: 348428af-afa7-4ff3-b571-acf874301cf2
ms.openlocfilehash: 663d05ef482a97b4ac33664ab62f1556e62763a6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97119100"
---
# <a name="__identifier-ccli"></a>__identifier (C++/CLI)

Разрешает использование ключевых слов C++ в качестве идентификаторов.

## <a name="all-platforms"></a>Все платформы

### <a name="syntax"></a>Синтаксис

```cpp
__identifier(C++_keyword)
```

### <a name="remarks"></a>Remarks

Разрешено использование ключевого слова **__identifier** для идентификаторов, которые не являются ключевыми словами. Но такой вариант настоятельно не рекомендуется использовать из-за стиля.

## <a name="windows-runtime"></a>Среда выполнения Windows

### <a name="requirements"></a>Требования

Параметр компилятора: `/ZW`

### <a name="examples"></a>Примеры

**Пример**

В следующем примере класс с именем `template` создается в C# и распространяется в виде библиотеки DLL. В программе C++/CLI, использующей `template` класс, **`__identifier`** ключевое слово скрывает тот факт, что `template` является стандартным ключевым словом C++.

```csharp
// identifier_template.cs
// compile with: /target:library
public class template {
   public void Run() { }
}
```

```cpp
// keyword__identifier.cpp
// compile with: /ZW
#using <identifier_template.dll>
int main() {
   __identifier(template)^ pTemplate = ref new __identifier(template)();
   pTemplate->Run();
}
```

## <a name="common-language-runtime"></a>Среда CLR

### <a name="remarks"></a>Комментарии

Ключевое слово **__Identifier** может использоваться с параметром компилятора `/clr`.

### <a name="requirements"></a>Требования

Параметр компилятора: `/clr`

### <a name="examples"></a>Примеры

В следующем примере класс с именем `template` создается в C# и распространяется в виде библиотеки DLL. В программе C++/CLI, использующей `template` класс, **`__identifier`** ключевое слово скрывает тот факт, что `template` является стандартным ключевым словом C++.

```csharp
// identifier_template.cs
// compile with: /target:library
public class template {
   public void Run() { }
}
```

```cpp
// keyword__identifier.cpp
// compile with: /clr
#using <identifier_template.dll>

int main() {
   __identifier(template) ^pTemplate = gcnew __identifier(template)();
   pTemplate->Run();
}
```

## <a name="see-also"></a>См. также раздел

[Расширения компонентов для .NET и UWP](component-extensions-for-runtime-platforms.md)<br/>
[Расширения компонентов для .NET и UWP](component-extensions-for-runtime-platforms.md)
