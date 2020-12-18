---
description: 'Подробнее о следующем: Автоматизация в библиотеке DLL'
title: Автоматизация в библиотеке DLL
ms.date: 11/04/2016
helpviewer_keywords:
- DLLs [C++], Automation
- Automation [C++], DLLs
ms.assetid: 2728ecd1-14e2-4ae0-a946-e749e11dbb74
ms.openlocfilehash: e0d6d0beec71f3994f6e726c6946b2069d1b081b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97163240"
---
# <a name="automation-in-a-dll"></a>Автоматизация в библиотеке DLL

При выборе параметра "Автоматизация" в мастере библиотек DLL MFC мастер предоставляет следующее:

- Файл языка описания начального объекта (ODL)

- Директива include в файле STDAFX h для Afxole.h

- Реализация функции `DllGetClassObject`, которая вызывает функцию **AfxDllGetClassObject**

- Реализация функции `DllCanUnloadNow`, которая вызывает функцию **AfxDllCanUnloadNow**

- Реализация функции `DllRegisterServer`, которая вызывает функцию [COleObjectFactory::UpdateRegistryAll](../mfc/reference/coleobjectfactory-class.md#updateregistryall)

## <a name="what-do-you-want-to-know-more-about"></a>Дополнительные сведения

- [Серверы автоматизации](../mfc/automation-servers.md)

## <a name="see-also"></a>См. также

[Создание библиотек DLL C/C++ в Visual Studio](dlls-in-visual-cpp.md)
