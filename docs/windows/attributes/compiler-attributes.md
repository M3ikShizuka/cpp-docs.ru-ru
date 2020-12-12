---
description: 'Дополнительные сведения: атрибуты компилятора'
title: Атрибуты компилятора (C++ COM)
ms.date: 10/02/2018
helpviewer_keywords:
- cl.exe compiler, attributes
- attributes [C++/CLI], compiler
ms.assetid: 53cd9bee-1521-48ec-b171-80feac2096cc
ms.openlocfilehash: 6d2cbb6bcffb5108ec98fe2786f9fb2216a79b9f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97306538"
---
# <a name="compiler-attributes"></a>Атрибуты компилятора

Атрибуты компилятора предоставляют различные функциональные возможности.

|Атрибут|Описание|
|---------------|-----------------|
|[emitidl](emitidl.md)|Определяет, будут ли обрабатываться все последующие атрибуты IDL и помещены в созданный IDL-файл.|
|[event_receiver](event-receiver.md)|Создает приемник событий.|
|[event_source](event-source.md)|Создает источник событий.|
|[программе](export.md)|Приводит к размещению структуры данных в IDL-файле.|
|[внедрен](implements-cpp.md)|Указывает интерфейсы диспетчеризации, которые должны быть членами coclass-класса IDL.|
|[importidl](importidl.md)|Вставляет указанный IDL-файл в созданный IDL-файл.|
|[importlib](importlib.md)|Делает типы, которые уже были скомпилированы в другую библиотеку типов, доступными для создаваемой библиотеки типов.|
|[инклуделиб](includelib-cpp.md)|Вызывает включение IDL-или h-файла в созданный IDL-файл.|
|[library_block](library-block.md)|Помещает конструкцию внутрь блока библиотеки IDL-файла.|
|[no_injected_text](no-injected-text.md)|Не позволяет компилятору внедрять код в результате использования атрибута.|
|[satype](satype.md)|Указывает тип данных `SAFEARRAY` .|
|[version](version-cpp.md)|Определяет определенную версию для нескольких версий интерфейса или класса.|

## <a name="see-also"></a>См. также раздел

[Атрибуты по группам](attributes-by-group.md)
