---
description: 'Дополнительные сведения о: Ошибка компилятора C3445'
title: Ошибка компилятора C3445
ms.date: 04/10/2017
f1_keywords:
- C3445
helpviewer_keywords:
- C3445
ms.assetid: 0d272bfc-136b-4025-a9ba-5e4eea5f8215
ms.openlocfilehash: 992c0e4f6e8b068bf6c038a6a5f58b45dd80a3c6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97316040"
---
# <a name="compiler-error-c3445"></a>Ошибка компилятора C3445

> Copy-List-инициализация "*тип*" не может использовать явный конструктор

Согласно стандарту ISO C++ 17, компилятору необходимо рассмотреть явный конструктор для разрешения перегрузки при инициализации копирования списка, но если эта перегрузка фактически выбрана, необходимо вызвать ошибку.

Начиная с Visual Studio 2017 компилятор обнаруживает ошибки, связанные с созданием объектов, с помощью списка инициализаторов, который не был найден в Visual Studio 2015. Эти ошибки могут привести к сбоям или неопределенному поведению во время выполнения.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C3445.

```cpp
// C3445.cpp
struct A
{
    explicit A(int) {}
    A(double) {}
};

int main()
{
    A a1 = { 1 };     // error C3445: copy-list-initialization of
                      //     'A' cannot use an explicit constructor
}
```

Чтобы исправить эту ошибку, используйте вместо нее прямую инициализацию:

```cpp
// C3445b.cpp
struct A
{
    explicit A(int) {}
    A(double) {}
};

int main()
{
    A a1{ 1 };
}
```
