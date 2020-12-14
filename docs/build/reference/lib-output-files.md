---
description: 'Дополнительные сведения: выходные файлы LIB'
title: Выходные LIB-файлы
ms.date: 11/04/2016
helpviewer_keywords:
- output files, LIB
ms.assetid: e73d2f9b-a42d-402b-b7e3-3a94bebb317e
ms.openlocfilehash: 5a9145f4c75db0c402bc4416cedfd6d63bb23cd4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97191073"
---
# <a name="lib-output-files"></a>Выходные LIB-файлы

Выходные файлы, создаваемые библиотекой LIB, зависят от режима, в котором они используются, как показано в следующей таблице.

|Режим|Выходные данные|
|----------|------------|
|По умолчанию (сборка или изменение библиотеки)|Библиотека COFF (. lib)|
|Извлечение члена с помощью/EXTRACT|Файл объекта (obj)|
|Создание файла экспорта и импорт библиотеки с помощью/DEF|Импорт библиотеки (lib) и файла экспорта (exp)|

## <a name="see-also"></a>См. также раздел

[Общие сведения о LIB](overview-of-lib.md)
