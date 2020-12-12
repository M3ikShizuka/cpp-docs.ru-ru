---
description: Дополнительные сведения:. ILK в качестве входных файлов компоновщика
title: ILK-файлы в качестве входных файлов компоновщика
ms.date: 11/04/2016
helpviewer_keywords:
- ILK files
- .ilk files
ms.assetid: 7324c104-9e5d-423d-b268-b59f92607bf2
ms.openlocfilehash: 0aaa5fac19cedb8d94fc6dc9ab03a0f23fa0e49b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97192737"
---
# <a name="ilk-files-as-linker-input"></a>ILK-файлы в качестве входных файлов компоновщика

При добавочной компоновке LINK обновляет файл состояния ILK, созданный во время первой добавочной ссылки. Этот файл имеет то же базовое имя, что и exe-файл или DLL-файл, и имеет расширение ILK. При последующих добавочных ссылках LINK обновляет ILK файл. Если ILK-файл отсутствует, LINK выполняет полную компоновку и создает новый ILK-файл. Если ILK-файл непригоден для использования, LINK выполняет неинкрементную ссылку. Дополнительные сведения о инкрементной компоновке см. в разделе [добавочная ссылка (/incremental)](incremental-link-incrementally.md) .

## <a name="see-also"></a>См. также раздел

[Входные файлы ссылок](link-input-files.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
