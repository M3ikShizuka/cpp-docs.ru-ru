---
description: Дополнительные сведения см. в статье Создание и использование экземпляров unique_ptr
title: Практическое руководство. Создание и использование экземпляров unique_ptr
ms.custom: how-to
ms.date: 11/19/2018
ms.topic: conceptual
ms.assetid: 9a373030-e587-452f-b9a5-c5f9d58b7673
ms.openlocfilehash: a53b3a9704c62803b50c9bde2c7db70c190a8008
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97268669"
---
# <a name="how-to-create-and-use-unique_ptr-instances"></a>Практическое руководство. Создание и использование экземпляров unique_ptr

[Unique_ptr](../standard-library/unique-ptr-class.md) не имеет общего доступа к указателю. Его нельзя скопировать в другую `unique_ptr` , передать по значению в функцию или использовать в любом алгоритме стандартной библиотеки C++, для которого требуется выполнить копирование. `unique_ptr` можно только переместить. Это означает, что владение ресурсов памяти переносится в другое `unique_ptr` и оригинал `unique_ptr` больше им не владеет. Рекомендуется ограничить объект одним владельцем, поскольку множественное владение усложняет логику программы. Поэтому, если требуется интеллектуальный указатель для простого объекта C++, используйте `unique_ptr` , а при создании `unique_ptr` используйте вспомогательную функцию [make_unique](../standard-library/memory-functions.md#make_unique) .

Следующая схема иллюстрирует передачу прав собственности между двумя экземплярами `unique_ptr`.

![Перемещение владельца уникального&#95;PTR](media/unique_ptr.png "Перемещение владельца уникального&#95;PTR")

`unique_ptr` определяется в `<memory>` заголовке в стандартной библиотеке C++. Она точно так же эффективна, что и необработанный указатель, и может использоваться в контейнерах стандартной библиотеки C++. Добавление `unique_ptr` экземпляров в контейнеры стандартной библиотеки C++ является эффективным, так как конструктор перемещения объекта `unique_ptr` исключает необходимость в операции копирования.

## <a name="example-1"></a>Пример 1

В следующем примере описывается порядок создания экземпляров `unique_ptr` и передачи их между функциями.

[!code-cpp[stl_smart_pointers#210](codesnippet/CPP/how-to-create-and-use-unique-ptr-instances_1.cpp)]

В этих примерах демонстрируется эта базовая характеристика `unique_ptr`: ее можно изменить, но не для копирования. "Перемещение" перемещает владельца в новый `unique_ptr` и сбрасывает старый `unique_ptr`.

## <a name="example-2"></a>Пример 2

В следующем примере описывается порядок создания экземпляров `unique_ptr` и их использования в векторе.

[!code-cpp[stl_smart_pointers#211](codesnippet/CPP/how-to-create-and-use-unique-ptr-instances_2.cpp)]

Обратите внимание, что в диапазоне для цикла `unique_ptr` передается по ссылке. При попытке передачи по значению компилятор выдаст ошибку, поскольку конструктор копирования `unique_ptr` удален.

## <a name="example-3"></a>Пример 3

В следующем примере показана инициализация `unique_ptr`, являющегося членом класса.

[!code-cpp[stl_smart_pointers#212](codesnippet/CPP/how-to-create-and-use-unique-ptr-instances_3.cpp)]

## <a name="example-4"></a>Пример 4

[Make_unique](../standard-library/memory-functions.md#make_unique) можно использовать для создания `unique_ptr` массива, но нельзя использовать `make_unique` для инициализации элементов массива.

[!code-cpp[stl_smart_pointers#213](codesnippet/CPP/how-to-create-and-use-unique-ptr-instances_4.cpp)]

Дополнительные примеры см. в разделе [make_unique](../standard-library/memory-functions.md#make_unique).

## <a name="see-also"></a>См. также раздел

[Смарт-указатели (современный C++)](smart-pointers-modern-cpp.md)<br/>
[make_unique](../standard-library/memory-functions.md#make_unique)
