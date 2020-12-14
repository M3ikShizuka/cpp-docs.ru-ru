---
description: 'Дополнительные сведения: поддержка компоновщика для Delay-Loadedных библиотек DLL'
title: Поддержка компоновщика для DLLs, загружаемых с задержкой
ms.date: 11/04/2016
helpviewer_keywords:
- delayed loading of DLLs, linker support
ms.assetid: b2d7e449-2809-42b1-9c90-2c0ca5e31a14
ms.openlocfilehash: 6bf4527d14c7313874f162f0597114132b1a81cb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97190969"
---
# <a name="linker-support-for-delay-loaded-dlls"></a>Поддержка компоновщика для DLLs, загружаемых с задержкой

Компоновщик КОМПИЛЯТОРОМ MSVC теперь поддерживает отложенную загрузку библиотек DLL. Это освобождает вас от необходимости использовать функции Windows SDK **LoadLibrary** и **GetProcAddress** для реализации отложенной загрузки DLL.

До Visual C++ 6,0 единственным способом загрузки библиотеки DLL во время выполнения было использование **LoadLibrary** и **GetProcAddress**; операционная система загрузит библиотеку DLL при загрузке исполняемого файла или библиотеки DLL с ее помощью.

Начиная с Visual C++ 6,0, при неявной компоновке с библиотекой DLL компоновщик предоставляет параметры для задержки загрузки библиотеки DLL до тех пор, пока программа не вызовет функцию в этой библиотеке DLL.

Приложение может задержать загрузку библиотеки DLL с помощью параметра компоновщика [параметр/DELAYLOAD (отложенная загрузка импорта)](delayload-delay-load-import.md) с вспомогательной функцией (реализация по умолчанию, предоставляемая Visual C++). Вспомогательная функция будет загружать библиотеку DLL во время выполнения, вызывая **LoadLibrary** и **GetProcAddress** .

Рекомендуется задержать загрузку библиотеки DLL, если:

- Программа не может вызвать функцию в библиотеке DLL.

- Функция в библиотеке DLL может не вызываться до окончания выполнения программы.

Отложенная загрузка библиотеки DLL может быть указана во время сборки. EXE или. Проект библиотеки DLL. Конкретного. Проект DLL, который задерживает загрузку одной или нескольких библиотек DLL, не должен вызывать в DllMain точку входа, загруженную с задержкой.

В следующих разделах описываются отложенная загрузка библиотек DLL:

- [Указание библиотек DLL для задержки загрузки](specifying-dlls-to-delay-load.md)

- [Явная выгрузка библиотеки DLL Delay-Loaded](explicitly-unloading-a-delay-loaded-dll.md)

- [Загрузка всех импортов для Delay-Loaded DLL](loading-all-imports-for-a-delay-loaded-dll.md)

- [Импорт привязок](binding-imports.md)

- [Обработка ошибок и уведомление](error-handling-and-notification.md)

- [Дамп Delay-Loaded импортов](dumping-delay-loaded-imports.md)

- [Ограничения отложенной загрузки библиотек DLL](constraints-of-delay-loading-dlls.md)

- [Основные сведения о вспомогательной функции](understanding-the-helper-function.md)

- [Разработка собственной вспомогательной функции](developing-your-own-helper-function.md)

## <a name="see-also"></a>См. также

[Создание библиотек DLL C/C++ в Visual Studio](../dlls-in-visual-cpp.md)<br/>
[Справочник по компоновщику MSVC](linking.md)
