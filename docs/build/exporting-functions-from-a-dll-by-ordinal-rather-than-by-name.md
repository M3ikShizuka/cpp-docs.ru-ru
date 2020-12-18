---
description: 'Подробнее о следующем: Экспорт функций из библиотеки DLL по порядковому номеру, а не по имени'
title: Экспорт функций из библиотеки DLL по порядковому номеру, а не по имени
ms.date: 11/04/2016
helpviewer_keywords:
- exporting functions [C++], ordinal values
- ordinal exports [C++]
- exporting DLLs [C++], ordinal values
- NONAME attribute
ms.assetid: 679719fd-d965-4df3-9f7a-7d86ad831702
ms.openlocfilehash: 84d200e2c37161d6bef3e64e72130204640088c8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97156506"
---
# <a name="exporting-functions-from-a-dll-by-ordinal-rather-than-by-name"></a>Экспорт функций из библиотеки DLL по порядковому номеру, а не по имени

Самый простой способ экспортировать функции из библиотеки DLL — экспортировать их по имени. Это происходит, например, при использовании **`__declspec(dllexport)`** . Но также можно экспортировать функции по порядковому номеру. При использовании этого метода необходимо использовать DEF-файл вместо **`__declspec(dllexport)`** . Чтобы указать порядковое значение функции, добавьте ее порядковый номер в имя функции в DEF-файле. Сведения об указании порядковых номеров см. в разделе [Экспорт из библиотеки DLL с помощью DEF-файлов](exporting-from-a-dll-using-def-files.md).

> [!TIP]
> Если требуется оптимизировать размер файла библиотеки DLL, используйте атрибут **NONAME** для каждой экспортированной функции. При использовании атрибута **NONAME** порядковые номера хранятся в таблице экспорта библиотеки DLL, а не в именах функций. Это поможет значительно сэкономить при экспорте множества функций.

## <a name="what-do-you-want-to-do"></a>Выберите действие

- [Использовать DEF-файл для экспорта по порядковому номеру](exporting-from-a-dll-using-def-files.md)

- [Использовать __declspec(dllexport)](exporting-from-a-dll-using-declspec-dllexport.md)

## <a name="see-also"></a>См. также

[Экспорт из библиотеки DLL](exporting-from-a-dll.md)
