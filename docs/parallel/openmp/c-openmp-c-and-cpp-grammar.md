---
description: 'Дополнительные сведения: C. грамматика OpenMP C и C++'
title: В. Грамматика OpenMP C и C++
ms.date: 01/16/2019
ms.assetid: 97a878ce-1533-47f7-a134-66fcbff48524
ms.openlocfilehash: 9543d721afbff1069b5497ba8dc7092089a1b706
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97342508"
---
# <a name="c-openmp-c-and-c-grammar"></a>В. Грамматика OpenMP C и C++

[C.1 Нотация](#c1-notation)<br/>
[C.2 Правила](#c2-rules)

## <a name="c1-notation"></a>C.1 Нотация

Правила грамматики состоят из имени для нетерминального, за которым следует двоеточие, а затем альтернативные варианты замены в отдельных строках.

Термин «выражение синтаксиса<sub>» указывает, что термин является</sub> необязательным в пределах замены.

*Выражение синтаксиса Expression*<sub>оптсек</sub> эквивалентно значению *ключевого слова-seq*<sub>OPT</sub> со следующими дополнительными правилами:

*Term — seq*:  
&nbsp;&nbsp;&nbsp;&nbsp;*термин*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;терм *— Seq* <br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Term-seq* `,` *срок*   

## <a name="c2-rules"></a>C.2 Правила

Нотация описана в разделе 6,1 стандарта C. В этом грамматическом приложении показаны расширения для грамматики базового языка для директив OpenMP C и C++.

**/\* в C++ (ISO/IEC 14882:1998) \*/**

*оператор-seq*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*statement*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Директива OpenMP*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Инструкция-Seq, инструкция*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Оператор-последовательность OpenMP-директива*

**/\* в C90 (ISO/IEC 9899:1990) \*/**

*statement-list*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*statement*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Директива OpenMP*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Statement-оператор List*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Инструкция-список директив OpenMP*

**/\* в C99 (ISO/IEC 9899:1999) \*/**

*блочный элемент*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*declaration*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*statement*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Директива OpenMP*

**/\* стандартные операторы \*/**

*statement*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Конструкция OpenMP*

*конструкция OpenMP*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Параллельная конструкция*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*for-конструкция*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*раздел — конструкция*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*одиночная конструкция*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Parallel-for-конструкция*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Конструкция Parallel-Sections*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Главная — конструкция*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Критическая — конструкция*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Атомарная конструкция*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*упорядоченная конструкция*

*директива OpenMP*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*барьер-директива*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*flush-директива*

*структурированный блок*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*statement*

*параллельная конструкция*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*структурированный блок директивы parallel*

*директива parallel-*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `# pragma omp parallel`*Parallel-предложение*<sub>оптсек</sub> *New-Line*

*Parallel-предложение*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Unique — параллельное предложение*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Data-предложение*

*UNIQUE — параллельное предложение*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `if (`*выражение*   `)`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `num_threads (`*выражение*   `)`

*для конструкции*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Оператор итерации for-директивы*

*директива for*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `# pragma omp for`*for-предложение*<sub>оптсек</sub> *New-Line*

*предложение for*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Unique-for-предложение*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Data-предложение*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `nowait`

*UNIQUE-предложение-for*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `ordered`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `schedule (`*Тип расписания*   `)`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `schedule (`*Тип расписания* `,` *выражение*      `)`

*Тип расписания*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `static`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `dynamic`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `guided`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `runtime`

*Создание разделов*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*область раздела директивы разделов*

*директива Sections-*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `# pragma omp sections`*раздел — предложение*<sub>оптсек</sub> *New-Line*

*предложение Sections*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Data-предложение*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `nowait`

*область видимости раздела*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*{Section-Sequence}*

*последовательность разделов*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*директива раздела —*<sub></sub> *структурный блок*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*раздел-структура-директива раздела последовательности*

*директива Section*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `# pragma omp section`*Новая строка*

*одиночная конструкция*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*структурированный блок с одной директивой*

*одна директива*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `# pragma omp single`оптсек с *одним предложением*<sub></sub> *New-Line*

*одно предложение*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Data-предложение*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `nowait`

*Parallel-for-конструкция*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Оператор parallel-for-директива-Инструкция*

*Parallel-for-директива*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `# pragma omp parallel for`*Parallel-for-предложение*<sub>оптсек</sub> *New-Line*

*Parallel-for-предложение*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Unique — параллельное предложение*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Unique-for-предложение*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Data-предложение*

*конструкция Parallel-Sections*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*раздел директивы parallel-Sections-Scope*

*директива parallel-Sections-*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `# pragma omp parallel sections`*Parallel-Sections-предложение*<sub>оптсек</sub> *New-Line*

*предложение Parallel-Sections*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Unique — параллельное предложение*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Data-предложение*

*Главная — конструкция*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*структурный блок в директиве Master-*

*Основная директива*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `# pragma omp master`*Новая строка*

*Критическая — конструкция*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Ключевая директива с ключевым блоком*

*критическая директива*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `# pragma omp critical`*регион — фраза*<sub></sub> " *создать" — строка*

*регион — фраза*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Идентификатор*

*барьер — директива*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `# pragma omp barrier`*Новая строка*

*Атомарная конструкция*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*Оператор выражения-директивы atomic*

*атомарная директива*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `# pragma omp atomic`*Новая строка*

*директива flush*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `# pragma omp flush`*flush-переменных —*<sub></sub> *Новая строка*

*переменных*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*(Variable-List)*

*упорядоченная конструкция*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*структурированная директива Structured-Block*

*упорядоченная директива*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `# pragma omp ordered`*Новая строка*

**/\* стандартные объявления \*/**

*declaration*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*threadprivate-директива*

*threadprivate-директива*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `# pragma omp threadprivate (`*список переменных* `)` *Новая строка*    

*предложение данных*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `private (`*список переменных*   `)`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `copyprivate (`  *список переменных*    `)`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `firstprivate (`  *список переменных*    `)`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `lastprivate (`*список переменных*    `)`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `shared (`*список переменных*   `)`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `default ( shared )`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `default ( none )`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `reduction (`  *reduction-оператор* `:` *список переменных*          `)`<br/>
&nbsp;&nbsp;&nbsp;&nbsp;  `copyin (`  *список переменных*    `)`

*сокращение — оператор*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;Одно из следующих:   `+ \* - & ^ | && ||`

**/\* в C \*/**

*список переменных*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*identifier*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*список переменных* `,` *идентификатор*   

**/\* в C++ \*/**

*список переменных*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*ID-выражение*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*список переменных* `,` *ID-выражение*   
