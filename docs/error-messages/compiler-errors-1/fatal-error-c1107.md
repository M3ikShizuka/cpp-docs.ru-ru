---
description: 'Дополнительные сведения о: Неустранимая ошибка C1107'
title: Неустранимая ошибка C1107
ms.date: 11/04/2016
f1_keywords:
- C1107
helpviewer_keywords:
- C1107
ms.assetid: 541a4d9f-10bc-4dd8-b68e-15e548f3dc0a
ms.openlocfilehash: c746bcf5f8bcb0247d8603b1734a3b1bdbc174f1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97144914"
---
# <a name="fatal-error-c1107"></a>Неустранимая ошибка C1107

не удалось найти сборку "файл": укажите путь поиска сборок с помощью переключателя/AI или переменной среды LIBPATH

Файл метаданных был передан в директиву [#using](../../preprocessor/hash-using-directive-cpp.md) , которую компилятору не удалось разместить.

Переменная среды LIBPATH, описанная в разделе для `#using` , и параметр компилятора [/AI](../../build/reference/ai-specify-metadata-directories.md) позволяют указать каталоги, в которых компилятор будет искать файлы метаданных, на которые имеются ссылки.
