---
description: 'Дополнительные сведения: использование лямбда-выражений, объектов функций и ограниченных функций'
title: Использование лямбда-выражений, объектов функций и ограниченных функций
ms.date: 11/04/2016
ms.assetid: 25346cc9-869d-4ada-aad3-e2228cad3d6c
ms.openlocfilehash: bef02f30b5d5b5f11b8051c7a596ac0a141eef0a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97314455"
---
# <a name="using-lambdas-function-objects-and-restricted-functions"></a>Использование лямбда-выражений, объектов функций и ограниченных функций

Код C++ AMP, который вы хотите запустить в сочетании с ускорителем, указывается в качестве аргумента в вызове метода [parallel_for_each](reference/concurrency-namespace-functions-amp.md#parallel_for_each) . В качестве этого аргумента можно указать лямбда-выражение или объект функции (функтор). Кроме того, лямбда-выражение или объект функции может вызывать функцию с ограничениями C++ AMP. В этом разделе используется алгоритм сложения массивов для демонстрации лямбда-выражений, объектов функций и ограниченных функций. В следующем примере показан алгоритм без C++ AMP кода. 2 1 — создаются массивы с одинаковой длиной. Соответствующие целочисленные элементы добавляются и хранятся в третьем одномерном массиве. C++ AMP не используется.

```cpp
void CpuMethod() {

    int aCPP[] = {1, 2, 3, 4, 5};
    int bCPP[] = {6, 7, 8, 9, 10};
    int sumCPP[5];

    for (int idx = 0; idx <5; idx++)
    {
        sumCPP[idx] = aCPP[idx] + bCPP[idx];
    }

    for (int idx = 0; idx <5; idx++)
    {
        std::cout <<sumCPP[idx] <<"\n";
    }
}
```

## <a name="lambda-expression"></a>Лямбда-выражение

Использование лямбда-выражения является наиболее прямым способом использования C++ AMP для перезаписи кода.

```cpp
void AddArraysWithLambda() {
    int aCPP[] = {1, 2, 3, 4, 5};
    int bCPP[] = {6, 7, 8, 9, 10};
    int sumCPP[5];

    array_view<const int, 1> a(5, aCPP);

    array_view<const int, 1> b(5, bCPP);

    array_view<int, 1> sum(5, sumCPP);

    sum.discard_data();

    parallel_for_each(
        sum.extent,
        [=](index<1> idx) restrict(amp)
        {
             sum[idx] = a[idx] + b[idx];
        });

    for (int i = 0; i <5; i++) {
        std::cout <<sum[i] <<"\n";
    }
}
```

Лямбда-выражение должно включать один параметр индексирования и должно включать `restrict(amp)` . В этом примере объект [array_view](../../parallel/amp/reference/array-view-class.md) `sum` имеет ранг 1. Поэтому параметр для лямбда-оператора является объектом [индекса](../../parallel/amp/reference/index-class.md) , который имеет ранг 1. Во время выполнения лямбда-выражение выполняется один раз для каждого элемента в объекте [array_view](../../parallel/amp/reference/array-view-class.md) . Дополнительные сведения см. в разделе [синтаксис лямбда-выражений](../../cpp/lambda-expression-syntax.md).

## <a name="function-object"></a>Объект Function

Код ускорителя можно разделить на объект функции.

```cpp
class AdditionFunctionObject
{
public:
    AdditionFunctionObject(const array_view<int, 1>& a,
    const array_view<int, 1>& b,
    const array_view<int, 1>& sum)
    : a(a), b(b), sum(sum)
    {
    }

    void operator()(index<1> idx) restrict(amp)
    {
        sum[idx] = a[idx] + b[idx];
    }

private:
    array_view<int, 1> a;
    array_view<int, 1> b;
    array_view<int, 1> sum;
};

void AddArraysWithFunctionObject() {
    int aCPP[] = {1, 2, 3, 4, 5};
    int bCPP[] = {6, 7, 8, 9, 10};
    int sumCPP[5];

    array_view<const int, 1> a(5, aCPP);

    array_view<const int, 1> b(5, bCPP);

    array_view<int, 1> sum(5, sumCPP);

    sum.discard_data();

    parallel_for_each(
        sum.extent,
        AdditionFunctionObject(a, b, sum));

    for (int i = 0; i <5; i++) {
        std::cout <<sum[i] <<"\n";
    }
}
```

Объект функции должен включать конструктор и должен включать перегрузку оператора вызова функции. Оператор вызова функции должен включать один параметр индексирования. Экземпляр объекта функции передается в качестве второго аргумента методу [parallel_for_each](reference/concurrency-namespace-functions-amp.md#parallel_for_each) . В этом примере в конструктор объекта функции передается три [array_view](../../parallel/amp/reference/array-view-class.md) объектов. Объект [array_view](../../parallel/amp/reference/array-view-class.md) `sum` имеет ранг 1. Поэтому параметром для оператора вызова функции является объект [индекса](../../parallel/amp/reference/index-class.md) с рангом 1. Во время выполнения функция выполняется один раз для каждого элемента в объекте [array_view](../../parallel/amp/reference/array-view-class.md) . Дополнительные сведения см. в разделе [вызов функции](../../cpp/function-call-cpp.md) и [объекты функций в стандартной библиотеке C++](../../standard-library/function-objects-in-the-stl.md).

## <a name="c-amp-restricted-function"></a>Функция AMP-Restricted C++

Можно дополнительно разделить код ускорителя, создав функцию ограничения и вызвав ее из лямбда-выражения или объекта функции. В следующем примере кода показано, как вызвать ограниченную функцию из лямбда-выражения.

```cpp
void AddElementsWithRestrictedFunction(index<1> idx, array_view<int, 1> sum, array_view<int, 1> a, array_view<int, 1> b) restrict(amp)
{
    sum[idx] = a[idx] + b[idx];
}

void AddArraysWithFunction() {

    int aCPP[] = {1, 2, 3, 4, 5};
    int bCPP[] = {6, 7, 8, 9, 10};
    int sumCPP[5];

    array_view<int, 1> a(5, aCPP);

    array_view<int, 1> b(5, bCPP);

    array_view<int, 1> sum(5, sumCPP);

    sum.discard_data();

    parallel_for_each(
        sum.extent,
        [=](index<1> idx) restrict(amp)
        {
            AddElementsWithRestrictedFunction(idx, sum, a, b);
        });

    for (int i = 0; i <5; i++) {
        std::cout <<sum[i] <<"\n";
    }
}
```

Функция с ограничением должна включать `restrict(amp)` и соответствовать ограничениям, описанным в разделе [ограничение (C++ amp)](../../cpp/restrict-cpp-amp.md).

## <a name="see-also"></a>См. также раздел

[C++ AMP (C++ Accelerated Massive Parallelism)](../../parallel/amp/cpp-amp-cpp-accelerated-massive-parallelism.md)<br/>
[Синтаксис лямбда-выражений](../../cpp/lambda-expression-syntax.md)<br/>
[Вызов функции](../../cpp/function-call-cpp.md)<br/>
[Объекты функций в стандартной библиотеке C++](../../standard-library/function-objects-in-the-stl.md)<br/>
[restrict (C++ AMP)](../../cpp/restrict-cpp-amp.md)
