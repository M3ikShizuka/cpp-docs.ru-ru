---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4462'
title: Предупреждение компилятора (уровень 1) C4462
ms.date: 10/25/2017
f1_keywords:
- C4462
helpviewer_keywords:
- C4462
ms.assetid: 4e20aca4-293e-4c75-a83d-961c27ab7840
ms.openlocfilehash: 81696df228b2cbe6278521f602d2a6f986cacb13
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97212536"
---
# <a name="compiler-warning-level-1-c4462"></a>Предупреждение компилятора (уровень 1) C4462

> невозможно определить GUID типа. Программа может завершиться ошибкой во время выполнения.

Предупреждение C4462 возникает в приложении или компоненте среды выполнения Windows, когда открытый `TypedEventHandler` содержит в качестве одного из своих параметров типа ссылку на включающий класс.

Это предупреждение автоматически повышается до ошибки. Если вы хотите изменить это поведение, используйте [#pragma предупреждение](../../preprocessor/warning.md). Например, чтобы сделать C4462 проблемой с предупреждением уровня 4, добавьте следующую строку в файл исходного кода:

```cpp
#pragma warning(4:4462)
```

## <a name="example"></a>Пример

В этом примере создается предупреждение C4462:

```cpp
namespace N
{
    public ref struct EventArgs sealed {};
    public ref struct R sealed
    {
        R() {}
        event Windows::Foundation::TypedEventHandler<R ^, EventArgs^>^ e;
    };
}

[Platform::MTAThread]
int main()
{
    auto x = ref new N::R();
}
```

Существует два способа устранения этой ошибки. Одним из способов, который показан в следующем примере, является предоставление событию внутренней доступности, чтобы оно было доступно коду в этом же исполняемом файле, но не в коде других компонентов среды выполнения Windows.

```cpp
internal:
    event Windows::Foundation::TypedEventHandler<R ^, EventArgs^>^ e;
```

Если событие должно быть открытым, можно использовать другое решение, заключающееся в предоставлении доступа через интерфейс по умолчанию:

```cpp
ref struct R;
public interface struct IR{ event Windows::Foundation::TypedEventHandler<R ^, EventArgs^>^ e;};

public ref struct R sealed : [Windows::Foundation::Metadata::Default] IR
{
    R() {}
    virtual event Windows::Foundation::TypedEventHandler<R ^, EventArgs^>^ e;
};
```

Идентификатор GUID типа `Windows::Foundation::TypedEventHandler<R^, EventArgs^>^` используется только при обращении к этому типу из другого компонента. Первый способ работает, поскольку после исправления доступ возможен только из собственного компонента. В противном случае компилятор должен предположить наихудший случай и выдать предупреждение.
