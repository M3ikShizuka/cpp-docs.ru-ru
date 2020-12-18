---
description: 'Подробнее о следующем: Экспорт из библиотеки DLL'
title: Экспорт из библиотеки DLL
ms.date: 11/04/2016
helpviewer_keywords:
- exporting DLLs [C++], about exporting from DLLs
- exporting functions [C++], DLLs (exporting from)
- exporting DLLs [C++]
- DLLs [C++], exporting from
- DLL exports [C++]
- functions [C++], exporting
- exports table [C++]
ms.assetid: a08f86c4-5996-460b-ae54-da2b764045f0
ms.openlocfilehash: 324ca733eab48973dc9ca902f81abfe4ce52a5c6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97162941"
---
# <a name="exporting-from-a-dll"></a>Экспорт из библиотеки DLL

Файл DLL имеет макет, очень похожий на EXE-файл, с одним важным отличием — DLL-файл содержит таблицу экспорта. Таблица экспорта содержит имя каждой функции, которую библиотека DLL экспортирует в другие исполняемые файлы. Эти функции являются точками входа в библиотеку DLL; другие исполняемые файлы могут обращаться только к функциям из таблицы экспорта. Все остальные функции библиотеки DLL являются закрытыми. Таблицу экспорта библиотеки DLL можно просмотреть с помощью средства [DUMPBIN](reference/dumpbin-reference.md) с параметром /EXPORTS.

Экспортировать функции из библиотеки DLL можно двумя способами:

- Создайте файл определения модуля (DEF) и используйте DEF-файл при сборке библиотеки DLL. Используйте этот подход, если требуется [экспортировать функции из библиотеки DLL по порядковому номеру, а не по имени](exporting-functions-from-a-dll-by-ordinal-rather-than-by-name.md).

- Используйте ключевое слово **`__declspec(dllexport)`** в определении функции.

При экспорте функций любым способом убедитесь, что используется соглашение о вызовах [__stdcall](../cpp/stdcall.md).

## <a name="what-do-you-want-to-do"></a>Выберите действие

- [Экспорт из библиотеки DLL с использованием DEF-файлов](exporting-from-a-dll-using-def-files.md)

- [Экспорт из библиотеки DLL с использованием __declspec(dllexport)](exporting-from-a-dll-using-declspec-dllexport.md)

- [Экспорт и импорт с использованием AFX_EXT_CLASS](exporting-and-importing-using-afx-ext-class.md)

- [Экспорт функций на языке C++ для использования в исполняемых модулях, исходный код которых написан на языке C](exporting-cpp-functions-for-use-in-c-language-executables.md)

- [Экспорт функций на языке C для использования в исполняемых файлах, исходный код которых написан на языке C или C++](exporting-c-functions-for-use-in-c-or-cpp-language-executables.md)

- [Экспорт функций из библиотеки DLL по порядковому номеру, а не по имени](exporting-functions-from-a-dll-by-ordinal-rather-than-by-name.md)

- [Определение подходящего способа экспорта](determining-which-exporting-method-to-use.md)

- [Связывание исполняемого файла с библиотекой DLL](linking-an-executable-to-a-dll.md#determining-which-linking-method-to-use)

- [Инициализация библиотеки DLL](run-time-library-behavior.md#initializing-a-dll)

## <a name="what-do-you-want-to-know-more-about"></a>Дополнительные сведения

- [Импорт в приложение](importing-into-an-application.md)

- [Импорт и экспорт встраиваемых функций](importing-and-exporting-inline-functions.md)

- [Взаимный импорт](mutual-imports.md)

## <a name="see-also"></a>См. также

[Импортирование и экспортирование](importing-and-exporting.md)
