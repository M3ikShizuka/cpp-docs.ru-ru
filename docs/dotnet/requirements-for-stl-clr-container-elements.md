---
description: Дополнительные сведения о требованиях к элементам контейнера STL/CLR
title: Требования к элементам контейнера STL/CLR
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- C++ Standard Library, template class containers
- STL/CLR, containers
- containers, STL/CLR
- containers, C++ Standard Library
ms.assetid: 59ab240c-15bf-4701-a9f9-e7c56e5ab53f
ms.openlocfilehash: 3696d9df40f69b1dd39205a2dc7a3b802e815841
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97305511"
---
# <a name="requirements-for-stlclr-container-elements"></a>Требования к элементам контейнера STL/CLR

Все ссылочные типы, которые вставляются в контейнеры STL/CLR, должны иметь, как минимум, следующие элементы:

- Открытый конструктор копии.

- Открытый оператор присваивания.

- Открытый деструктор.

Кроме того, в ассоциативных контейнерах, таких как [Set](../dotnet/set-stl-clr.md) и [Map](../dotnet/map-stl-clr.md) , должен быть определен открытый оператор сравнения, который `operator<` по умолчанию имеет значение. Для некоторых операций с контейнерами также может потребоваться открытый конструктор по умолчанию и оператор открытого эквивалента.

Как и ссылочные типы, типы значений и дескрипторы ссылочных типов, которые вставляются в ассоциативный контейнер, должны иметь оператор сравнения, такой как `operator<` определенный. Требования к открытому конструктору копии, открытому оператору присваивания и открытому деструктору не существуют для типов значений или дескрипторов ссылочных типов.

## <a name="see-also"></a>См. также раздел

[Справочник по стандартной библиотеке C++](../standard-library/cpp-standard-library-reference.md)
