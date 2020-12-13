---
description: 'Дополнительные сведения о: A. examples'
title: A. Примеры
ms.date: 01/18/2019
ms.assetid: c0f6192f-a205-449b-b84c-cb30dbcc8b8f
ms.openlocfilehash: d52b59f9f83cf791c03fb49ca726273a2c977e58
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97342547"
---
# <a name="a-examples"></a>A. Примеры

Ниже приведены примеры конструкций, определенных в этом документе. Оператор, следующий за директивой, является составным только при необходимости, а несоставной оператор становится отступом от предшествующей директивы.

## <a name="a1-a-simple-loop-in-parallel"></a>A. 1 простой цикл в параллельном режиме

В следующем примере показано, как параллелизации цикла с помощью директивы [Parallel for](2-directives.md#251-parallel-for-construct) . По умолчанию переменная итерации цикла является закрытой, поэтому нет необходимости явно указывать ее в предложении Private.

```cpp
#pragma omp parallel for
    for (i=1; i<n; i++)
        b[i] = (a[i] + a[i-1]) / 2.0;
```

## <a name="a2-conditional-compilation"></a>A. 2. Условная компиляция

В следующих примерах показано использование условной компиляции с помощью макроса OpenMP [_OPENMP](2-directives.md#22-conditional-compilation). При компиляции OpenMP `_OPENMP` макрос определяется.

```cpp
# ifdef _OPENMP
    printf_s("Compiled by an OpenMP-compliant implementation.\n");
# endif
```

Определенный оператор препроцессора позволяет тестировать более одного макроса в одной директиве.

```cpp
# if defined(_OPENMP) && defined(VERBOSE)
    printf_s("Compiled by an OpenMP-compliant implementation.\n");
# endif
```

## <a name="a3-parallel-regions"></a>A. 3 параллельные регионы

Директиву [Parallel](2-directives.md#23-parallel-construct) можно использовать в параллельных программах с грубой детализацией. В следующем примере каждый поток в параллельной области определяет, на какой части глобального массива `x` будет работать, на основе номера потока:

```cpp
#pragma omp parallel shared(x, npoints) private(iam, np, ipoints)
{
    iam = omp_get_thread_num();
    np =  omp_get_num_threads();
    ipoints = npoints / np;
    subdomain(x, iam, ipoints);
}
```

## <a name="a4-the-nowait-clause"></a>A. 4 предложение WITH

Если в параллельной области имеется множество независимых циклов, можно [использовать предложение WITH, чтобы](2-directives.md#241-for-construct) избежать неявного барьера в конце `for` директивы, как показано ниже:

```cpp
#pragma omp parallel
{
    #pragma omp for nowait
        for (i=1; i<n; i++)
             b[i] = (a[i] + a[i-1]) / 2.0;
    #pragma omp for nowait
        for (i=0; i<m; i++)
            y[i] = sqrt(z[i]);
}
```

## <a name="a5-the-critical-directive"></a>A. 5. Критическая директива

Следующий пример включает несколько [критических](2-directives.md#262-critical-construct) директив. В примере показана модель очереди, в которой задача выдается из очереди и работает. Для защиты от многих потоков, использующих одну и ту же задачу, операция удаления из очереди должна находиться в `critical` разделе. Так как две очереди в этом примере независимы, они защищаются `critical` директивами с разными именами, *xaxis* и *yaxis*.

```cpp
#pragma omp parallel shared(x, y) private(x_next, y_next)
{
    #pragma omp critical ( xaxis )
        x_next = dequeue(x);
    work(x_next);
    #pragma omp critical ( yaxis )
        y_next = dequeue(y);
    work(y_next);
}
```

## <a name="a6-the-lastprivate-clause"></a>A. 6 предложение lastprivate

Правильное выполнение иногда зависит от значения, присваиваемого последней итерацией цикла переменной. Такие программы должны перечислять все такие переменные как аргументы в предложении [lastprivate](2-directives.md#2723-lastprivate) , чтобы значения переменных совпадали с тем, когда цикл выполняется последовательно.

```cpp
#pragma omp parallel
{
   #pragma omp for lastprivate(i)
      for (i=0; i<n-1; i++)
         a[i] = b[i] + b[i+1];
}
a[i]=b[i];
```

В предыдущем примере значение `i` в конце параллельной области будет равно `n-1` , как в случае с последовательным регистром.

## <a name="a7-the-reduction-clause"></a>A. 7 предложение сокращения

В следующем примере показано предложение [reduction](2-directives.md#2726-reduction) :

```cpp
#pragma omp parallel for private(i) shared(x, y, n) \
                         reduction(+: a, b)
    for (i=0; i<n; i++) {
        a = a + x[i];
        b = b + y[i];
    }
```

## <a name="a8-parallel-sections"></a>A. 8 параллельных секций

В следующем примере (для [раздела 2.4.2](2-directives.md#242-sections-construct)) функции *xaxis*, *yaxis* и *заксис* могут выполняться параллельно. Первая `section` директива является необязательной.  Все `section` директивы должны присутствовать в лексической области `parallel sections` конструкции.

```cpp
#pragma omp parallel sections
{
    #pragma omp section
        xaxis();
    #pragma omp section
        yaxis();
    #pragma omp section
        zaxis();
}
```

## <a name="a9-single-directives"></a>A. 9. одиночные директивы

В следующем примере показана директива [Single](2-directives.md#243-single-construct) . В этом примере только один поток (как правило, первый поток, вызывающий `single` директиву) выводит сообщение о ходе выполнения. Пользователь не должен делать никаких допущений, когда поток будет выполнять этот `single` раздел. Все остальные потоки пропускают `single` раздел и останавливаются в барьере в конце `single` конструкции. Если другие потоки могут продолжать работу, не дожидаясь потока, выполняющего `single` раздел, в `nowait` директиве можно указать предложение `single` .

```cpp
#pragma omp parallel
{
    #pragma omp single
        printf_s("Beginning work1.\n");
    work1();
    #pragma omp single
        printf_s("Finishing work1.\n");
    #pragma omp single nowait
        printf_s("Finished work1 and beginning work2.\n");
    work2();
}
```

## <a name="a10-sequential-ordering"></a>A. 10 последовательных упорядочений

[Упорядоченные разделы](2-directives.md#266-ordered-construct) полезны для последовательного упорядочения результатов работы, выполняемой параллельно. Следующая программа выводит индексы в последовательном порядке:

```cpp
#pragma omp for ordered schedule(dynamic)
    for (i=lb; i<ub; i+=st)
        work(i);
void work(int k)
{
    #pragma omp ordered
        printf_s(" %d", k);
}
```

## <a name="a11-a-fixed-number-of-threads"></a>A. 11. фиксированное число потоков

Некоторые программы используют фиксированное, предопределенное количество потоков для корректного выполнения.  Поскольку значение по умолчанию для динамической настройки количества потоков определяется реализацией, такие программы могут отключить возможность динамических потоков и явно задать число потоков для обеспечения переносимости. В следующем примере показано, как это сделать с помощью [omp_set_dynamic](3-run-time-library-functions.md#317-omp_set_dynamic-function)и [omp_set_num_threads](3-run-time-library-functions.md#311-omp_set_num_threads-function).

```cpp
omp_set_dynamic(0);
omp_set_num_threads(16);
#pragma omp parallel shared(x, npoints) private(iam, ipoints)
{
    if (omp_get_num_threads() != 16)
      abort();
    iam = omp_get_thread_num();
    ipoints = npoints/16;
    do_by_16(x, iam, ipoints);
}
```

В этом примере программа выполняется правильно только в том случае, если она выполняется 16 потоками. Если реализация не поддерживает 16 потоков, поведение этого примера определяется реализацией.

Число потоков, выполняющих параллельную область, остается постоянным во время параллельной области, независимо от параметра динамических потоков. Механизм динамических потоков определяет количество потоков, используемых в начале параллельной области, и сохраняет его в течение всего региона.

## <a name="a12-the-atomic-directive"></a>A. 12 Директива atomic

В следующем примере избегают состояния гонки (одновременное обновление элемента *x* на множество потоков) с помощью директивы [Atomic](2-directives.md#264-atomic-construct) :

```cpp
#pragma omp parallel for shared(x, y, index, n)
    for (i=0; i<n; i++)
    {
        #pragma omp atomic
            x[index[i]] += work1(i);
        y[i] += work2(i);
    }
```

Преимуществом использования `atomic` директивы в этом примере является то, что он позволяет параллельно обновлять два различных элемента x. Если вместо этого используется [критическая](2-directives.md#262-critical-construct) директива, все обновления элементов *x* выполняются последовательно (хотя и не в гарантированном порядке).

`atomic`Директива применяется только к оператору C или C++, непосредственно следующему за ним.  В результате элементы *y* не обновляются атомарно в этом примере.

## <a name="a13-a-flush-directive-with-a-list"></a>A. 13. Директива flush со списком

В следующем примере используется `flush` директива для синхронизации объектов типа "точка — точка" между парами потоков:

```cpp
int   sync[NUMBER_OF_THREADS];
float work[NUMBER_OF_THREADS];
#pragma omp parallel private(iam,neighbor) shared(work,sync)
{
    iam = omp_get_thread_num();
    sync[iam] = 0;
    #pragma omp barrier

    // Do computation into my portion of work array
    work[iam] = ...;

    //  Announce that I am done with my work
    // The first flush ensures that my work is
    // made visible before sync.
    // The second flush ensures that sync is made visible.
    #pragma omp flush(work)
    sync[iam] = 1;
    #pragma omp flush(sync)

    // Wait for neighbor
    neighbor = (iam>0 ? iam : omp_get_num_threads()) - 1;
    while (sync[neighbor]==0)
    {
        #pragma omp flush(sync)
    }

    // Read neighbor's values of work array
    ... = work[neighbor];
}
```

## <a name="a14-a-flush-directive-without-a-list"></a>A. 14 директива flush без списка

В следующем примере (для [раздела 2.6.5](2-directives.md#265-flush-directive)) различаются общие объекты, затрагиваемые `flush` директивой, без списка из общих объектов, которые не затрагиваются.

```cpp
// omp_flush_without_list.c
#include <omp.h>

int x, *p = &x;

void f1(int *q)
{
    *q = 1;
    #pragma omp flush
    // x, p, and *q are flushed
    //   because they are shared and accessible
    // q is not flushed because it is not shared.
}

void f2(int *q)
{
    #pragma omp barrier
    *q = 2;

    #pragma omp barrier
    // a barrier implies a flush
    // x, p, and *q are flushed
    //   because they are shared and accessible
    // q is not flushed because it is not shared.
}

int g(int n)
{
    int i = 1, j, sum = 0;
    *p = 1;

    #pragma omp parallel reduction(+: sum) num_threads(10)
    {
        f1(&j);
        // i, n and sum were not flushed
        //   because they were not accessible in f1
        // j was flushed because it was accessible
        sum += j;
        f2(&j);
        // i, n, and sum were not flushed
        //   because they were not accessible in f2
        // j was flushed because it was accessible
        sum += i + j + *p + n;
    }
    return sum;
}

int main()
{
}
```

## <a name="a15-the-number-of-threads-used"></a>A. 15 число используемых потоков

Рассмотрим следующий некорректный пример (для [раздела 3.1.2](3-run-time-library-functions.md#312-omp_get_num_threads-function)):

```cpp
np = omp_get_num_threads(); // misplaced
#pragma omp parallel for schedule(static)
    for (i=0; i<np; i++)
        work(i);
```

`omp_get_num_threads()`Вызов возвращает 1 в серийном фрагменте кода, поэтому *NP* всегда будет равняться 1 в предыдущем примере. Чтобы определить число потоков, которые будут развернуты для параллельной области, вызов должен находиться внутри параллельной области.

В следующем примере показано, как переписать эту программу без включения запроса на число потоков:

```cpp
#pragma omp parallel private(i)
{
    i = omp_get_thread_num();
    work(i);
}
```

## <a name="a16-locks"></a>A. 16 блокировок

В следующем примере (для [раздела 3,2](3-run-time-library-functions.md#32-lock-functions)) аргумент функции Lock должен иметь тип `omp_lock_t` , и нет необходимости очищать его.  Функции блокировки приводят к простою потоков при ожидании входа в первую критическую секцию, но для выполнения других задач во время ожидания входа во вторую.  `omp_set_lock`Функция блокирует, но `omp_test_lock` функция не позволяет `skip()` выполнять работу.

```cpp
// omp_using_locks.c
// compile with: /openmp /c
#include <stdio.h>
#include <omp.h>

void work(int);
void skip(int);

int main() {
   omp_lock_t lck;
   int id;

   omp_init_lock(&lck);
   #pragma omp parallel shared(lck) private(id)
   {
      id = omp_get_thread_num();

      omp_set_lock(&lck);
      printf_s("My thread id is %d.\n", id);

      // only one thread at a time can execute this printf
      omp_unset_lock(&lck);

      while (! omp_test_lock(&lck)) {
         skip(id);   // we do not yet have the lock,
                     // so we must do something else
      }
      work(id);     // we now have the lock
                    // and can do the work
      omp_unset_lock(&lck);
   }
   omp_destroy_lock(&lck);
}
```

## <a name="a17-nestable-locks"></a>A. 17 вложенные блокировки

В следующем примере (для [раздела 3,2](3-run-time-library-functions.md#32-lock-functions)) показано, как можно использовать вложенную блокировку для синхронизации обновлений как в целой структуре, так и в одном из ее членов.

```cpp
#include <omp.h>
typedef struct {int a,b; omp_nest_lock_t lck;} pair;

void incr_a(pair *p, int a)
{
    // Called only from incr_pair, no need to lock.
    p->a += a;
}

void incr_b(pair *p, int b)
{
    // Called both from incr_pair and elsewhere,
    // so need a nestable lock.

    omp_set_nest_lock(&p->lck);
    p->b += b;
    omp_unset_nest_lock(&p->lck);
}

void incr_pair(pair *p, int a, int b)
{
    omp_set_nest_lock(&p->lck);
    incr_a(p, a);
    incr_b(p, b);
    omp_unset_nest_lock(&p->lck);
}

void f(pair *p)
{
    extern int work1(), work2(), work3();
    #pragma omp parallel sections
    {
        #pragma omp section
            incr_pair(p, work1(), work2());
        #pragma omp section
            incr_b(p, work3());
    }
}
```

## <a name="a18-nested-for-directives"></a>A. 18 вложенных директив for

Следующий пример `for` [вложения директивы](2-directives.md#29-directive-nesting) является совместимым, так как внутренние и внешние `for` директивы привязаны к различным параллельным областям:

```cpp
#pragma omp parallel default(shared)
{
    #pragma omp for
        for (i=0; i<n; i++)
        {
            #pragma omp parallel shared(i, n)
            {
                #pragma omp for
                    for (j=0; j<n; j++)
                        work(i, j);
            }
        }
}
```

Следующий вариант предыдущего примера также соответствует требованиям:

```cpp
#pragma omp parallel default(shared)
{
    #pragma omp for
        for (i=0; i<n; i++)
            work1(i, n);
}

void work1(int i, int n)
{
    int j;
    #pragma omp parallel default(shared)
    {
        #pragma omp for
            for (j=0; j<n; j++)
                work2(i, j);
    }
    return;
}
```

## <a name="a19-examples-showing-incorrect-nesting-of-work-sharing-directives"></a>A. 19 примеры, демонстрирующие неправильное вложение директив совместного использования

В примерах этого раздела показаны правила [вложенности директив](2-directives.md#29-directive-nesting) .

Следующий пример не соответствует, так как внутренние и внешние `for` директивы являются вложенными и привязываются к одной и той же `parallel` директиве:

```cpp
void wrong1(int n)
{
  #pragma omp parallel default(shared)
  {
      int i, j;
      #pragma omp for
      for (i=0; i<n; i++) {
          #pragma omp for
              for (j=0; j<n; j++)
                 work(i, j);
     }
   }
}
```

Следующая динамически вложенная версия предыдущего примера также не соответствует требованиям:

```cpp
void wrong2(int n)
{
  #pragma omp parallel default(shared)
  {
    int i;
    #pragma omp for
      for (i=0; i<n; i++)
        work1(i, n);
  }
}

void work1(int i, int n)
{
  int j;
  #pragma omp for
    for (j=0; j<n; j++)
      work2(i, j);
}
```

Следующий пример не соответствует `for` `single` , поскольку директивы и являются вложенными и привязаны к одной параллельной области:

```cpp
void wrong3(int n)
{
  #pragma omp parallel default(shared)
  {
    int i;
    #pragma omp for
      for (i=0; i<n; i++) {
        #pragma omp single
          work(i);
      }
  }
}
```

Следующий пример не соответствует требованиям, поскольку `barrier` директива внутри `for` может привести к взаимоблокировке:

```cpp
void wrong4(int n)
{
  #pragma omp parallel default(shared)
  {
    int i;
    #pragma omp for
      for (i=0; i<n; i++) {
        work1(i);
        #pragma omp barrier
        work2(i);
      }
  }
}
```

Следующий пример не соответствует требованиям, поскольку `barrier` приводит к взаимоблокировке из-за того, что только один поток за раз может войти в критическую секцию:

```cpp
void wrong5()
{
  #pragma omp parallel
  {
    #pragma omp critical
    {
       work1();
       #pragma omp barrier
       work2();
    }
  }
}
```

Следующий пример не соответствует требованиям, поскольку `barrier` приводит к взаимоблокировке из-за того, что только один поток выполняет `single` раздел:

```cpp
void wrong6()
{
  #pragma omp parallel
  {
    setup();
    #pragma omp single
    {
      work1();
      #pragma omp barrier
      work2();
    }
    finish();
  }
}
```

## <a name="a20-bind-barrier-directives"></a>A. 20 директивы барьера привязки

Правила привязки директивы вызывают `barrier` директиву для привязки к ближайшей включающей `parallel` директиве. Дополнительные сведения о привязке директив см. в [разделе 2,8](2-directives.md#28-directive-binding).

В следующем примере вызов из *Main* в *sub2* соответствует требованиям, поскольку элемент `barrier` (в *sub3*) привязывается к параллельной области в *sub2*. Вызов из *Main* в *Sub1* соответствует требованиям, так как `barrier` привязывается к параллельной области в подподпрограмме *sub2*.  Вызов из *Main* в *sub3* соответствует требованиям, так как `barrier` не выполняет привязку к какой-либо параллельной области и игнорируется. Кроме того, `barrier` только синхронизирует группу потоков во внешней параллельной области, а не все потоки, созданные в *Sub1*.

```cpp
int main()
{
    sub1(2);
    sub2(2);
    sub3(2);
}

void sub1(int n)
{
    int i;
    #pragma omp parallel private(i) shared(n)
    {
        #pragma omp for
        for (i=0; i<n; i++)
            sub2(i);
    }
}

void sub2(int k)
{
     #pragma omp parallel shared(k)
     sub3(k);
}

void sub3(int n)
{
    work(n);
    #pragma omp barrier
    work(n);
}
```

## <a name="a21-scope-variables-with-the-private-clause"></a>A. 21 переменные области с предложением Private

Значения `i` и `j` в следующем примере не определены при выходе из параллельной области:

```cpp
int i, j;
i = 1;
j = 2;
#pragma omp parallel private(i) firstprivate(j)
{
  i = 3;
  j = j + 2;
}
printf_s("%d %d\n", i, j);
```

Дополнительные сведения о `private` предложении см. в [разделе 2.7.2.1](2-directives.md#2721-private).

## <a name="a22-the-defaultnone-clause"></a>A. 22. предложение default (None)

В следующем примере различаются переменные, затрагиваемые `default(none)` предложением из переменных, которые не являются:

```cpp
// openmp_using_clausedefault.c
// compile with: /openmp
#include <stdio.h>
#include <omp.h>

int x, y, z[1000];
#pragma omp threadprivate(x)

void fun(int a) {
   const int c = 1;
   int i = 0;

   #pragma omp parallel default(none) private(a) shared(z)
   {
      int j = omp_get_num_thread();
             //O.K.  - j is declared within parallel region
      a = z[j];       // O.K.  - a is listed in private clause
                      //      - z is listed in shared clause
      x = c;          // O.K.  - x is threadprivate
                      //      - c has const-qualified type
      z[i] = y;       // C3052 error - cannot reference i or y here

      #pragma omp for firstprivate(y)
         for (i=0; i<10 ; i++) {
            z[i] = y;  // O.K. - i is the loop control variable
                       // - y is listed in firstprivate clause
          }
       z[i] = y;   // Error - cannot reference i or y here
   }
}
```

Дополнительные сведения о `default` предложении см. в [разделе 2.7.2.5](2-directives.md#2725-default).

## <a name="a23-examples-of-the-ordered-directive"></a>A. 23 примеры директивы ordered

Можно иметь множество упорядоченных разделов с `for` указанным `ordered` предложением. Первый пример не соответствует требованиям, так как API задает следующее правило:

"Итерация цикла с `for` конструкцией не должна выполнять одну и ту же `ordered` директиву более одного раза и не должна выполнять более одной `ordered` директивы". (См. [раздел 2.6.6](2-directives.md#266-ordered-construct).)

В этом примере, не соответствующем требованиям, все итерации выполняют две упорядоченные секции:

```cpp
#pragma omp for ordered
for (i=0; i<n; i++)
{
    ...
    #pragma omp ordered
    { ... }
    ...
    #pragma omp ordered
    { ... }
    ...
}
```

В следующем примере, совместимом с, показано `for` более одного упорядоченного раздела:

```cpp
#pragma omp for ordered
for (i=0; i<n; i++)
{
    ...
    if (i <= 10)
    {
        ...
        #pragma omp ordered
        { ... }
    }
    ...
    (i > 10)
    {
        ...
        #pragma omp ordered
        { ... }
    }
    ...
}
```

## <a name="a24-example-of-the-private-clause"></a>A. 24. пример предложения Private

Предложение [Private](2-directives.md#2721-private) области Parallel действует только для лексического экстента области, а не для динамической области области.  Таким образом, в приведенном ниже примере любое использование переменной *a* в `for` цикле в подпрограммы *f* относится к закрытой копии, а использование в подпрограмме *g* относится к глобальному *а*.

```cpp
int a;

void f(int n)
{
    a = 0;

    #pragma omp parallel for private(a)
    for (int i=1; i<n; i++)
    {
        a = i;
        g(i, n);
        d(a);     // Private copy of "a"
        ...
    }
    ...

void g(int k, int n)
{
    h(k,a); // The global "a", not the private "a" in f
}
```

## <a name="a25-examples-of-the-copyprivate-data-attribute-clause"></a>A. 25 примеры предложения атрибута данных copyprivate

**Пример 1.** Предложение [copyprivate](2-directives.md#2728-copyprivate) можно использовать для передачи значений, получаемых одним потоком, непосредственно всем экземплярам частных переменных в других потоках.

```cpp
float x, y;
#pragma omp threadprivate(x, y)

void init( )
{
    float a;
    float b;

    #pragma omp single copyprivate(a,b,x,y)
    {
        get_values(a,b,x,y);
    }

    use_values(a, b, x, y);
}
```

Если метод *init* вызывается из последовательной области, его поведение не зависит от наличия директив. После вызова подпрограммы *get_values* в одном потоке ни один поток не покидает конструкцию до тех пор, пока закрытые объекты, обозначенные *a*, *b*, *x* и *y* во всех потоках, не будут определены с чтением значений.

**Пример 2:** В отличие от предыдущего примера, предположим, что чтение должно выполняться определенным потоком, скажем, главным потоком. В этом случае `copyprivate` предложение нельзя использовать для прямого вещания, но оно может использоваться для предоставления доступа к временному общему объекту.

```cpp
float read_next( )
{
    float * tmp;
    float return_val;

    #pragma omp single copyprivate(tmp)
    {
        tmp = (float *) malloc(sizeof(float));
    }

    #pragma omp master
    {
        get_float( tmp );
    }

    #pragma omp barrier
    return_val = *tmp;
    #pragma omp barrier

    #pragma omp single
    {
       free(tmp);
    }

    return return_val;
}
```

**Пример 3.** Предположим, что количество объектов блокировки, требуемых в параллельной области, не может быть легко определено перед вводом. `copyprivate`Предложение можно использовать для предоставления доступа к общим объектам блокировки, выделенным в пределах этой параллельной области.

```cpp
#include <omp.h>

omp_lock_t *new_lock()
{
    omp_lock_t *lock_ptr;

    #pragma omp single copyprivate(lock_ptr)
    {
        lock_ptr = (omp_lock_t *) malloc(sizeof(omp_lock_t));
        omp_init_lock( lock_ptr );
    }

    return lock_ptr;
}
```

## <a name="a26-the-threadprivate-directive"></a>A. 26 директива threadprivate

В следующих примерах демонстрируется использование директивы [threadprivate](2-directives.md#271-threadprivate-directive) для предоставления каждому потоку отдельного счетчика.

### <a name="example-1"></a>Пример 1

```cpp
int counter = 0;
#pragma omp threadprivate(counter)

int sub()
{
    counter++;
    return(counter);
}
```

### <a name="example-2"></a>Пример 2

```cpp
int sub()
{
    static int counter = 0;
    #pragma omp threadprivate(counter)
    counter++;
    return(counter);
}
```

## <a name="a27-c99-variable-length-arrays"></a>A. 27 C99 массивов переменной длины

В следующем примере показано, как использовать массивы C99 переменной длины (VLA) в директиве [фирстпривате](2-directives.md#2722-firstprivate) .

> [!NOTE]
> Массивы переменной длины в настоящее время не поддерживаются в Visual C++.

```cpp
void f(int m, int C[m][m])
{
    double v1[m];
    ...
    #pragma omp parallel firstprivate(C, v1)
    ...
}
```

## <a name="a28-the-num_threads-clause"></a>A. 28 предложение num_threads

В следующем примере демонстрируется предложение [num_threads](2-directives.md#23-parallel-construct) . Параллельная область выполняется с максимум 10 потоками.

```cpp
#include <omp.h>
main()
{
    omp_set_dynamic(1);
    ...
    #pragma omp parallel num_threads(10)
    {
        ... parallel region ...
    }
}
```

## <a name="a29-work-sharing-constructs-inside-a-critical-construct"></a>A. 29 конструкций совместного использования в критической конструкции

В следующем примере демонстрируется использование конструкции совместного использования внутри `critical` конструкции. Этот пример соответствует требованиям, поскольку конструкция совместного использования и `critical` конструкция не привязаны к одной параллельной области.

```cpp
void f()
{
  int i = 1;
  #pragma omp parallel sections
  {
    #pragma omp section
    {
      #pragma omp critical (name)
      {
        #pragma omp parallel
        {
          #pragma omp single
          {
            i++;
          }
        }
      }
    }
  }
}
```

## <a name="a30-reprivatization"></a>A. 30 Реприватизатион

В следующем примере демонстрируется реприватизатион переменных. Закрытые переменные могут быть помечены `private` повторно во вложенной директиве. Не нужно совместно использовать эти переменные во внешней параллельной области.

```cpp
int i, a;
...
#pragma omp parallel private(a)
{
  ...
  #pragma omp parallel for private(a)
  for (i=0; i<10; i++)
     {
       ...
     }
}
```

## <a name="a31-thread-safe-lock-functions"></a>A. 31 потокобезопасные функции блокировки

В следующем примере C++ показано, как инициализировать массив блокировок в параллельной области с помощью [omp_init_lock](3-run-time-library-functions.md#321-omp_init_lock-and-omp_init_nest_lock-functions).

```cpp
// A_13_omp_init_lock.cpp
// compile with: /openmp
#include <omp.h>

omp_lock_t *new_locks() {
   int i;
   omp_lock_t *lock = new omp_lock_t[1000];
   #pragma omp parallel for private(i)
   for (i = 0 ; i < 1000 ; i++)
      omp_init_lock(&lock[i]);

   return lock;
}

int main () {}
```
