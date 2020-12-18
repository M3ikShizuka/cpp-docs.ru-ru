---
description: 'Подробнее о следующем: Технология Active и библиотеки DLL'
title: Технология Active и библиотеки DLL
ms.date: 11/04/2016
helpviewer_keywords:
- in-process server DLLs
- Automation [C++], DLLs
- DLLs [C++], Active Technology
- Active technology [C++]
- MFC DLLs [C++], Active Technology
ms.assetid: 3ed27f8d-164a-4562-ad61-9f2333404cc7
ms.openlocfilehash: 02a11bd18e8c6f62748d0be3f4cd708c8e4e4621
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97157143"
---
# <a name="active-technology-and-dlls"></a>Технология Active и библиотеки DLL

Технология Active позволяет размещать серверы объектов внутри библиотеки DLL. Серверы такого типа называются внутрипроцессными. MFC не полностью поддерживает внутрипроцессный сервер для всех функций визуального редактирования, в основном потому, что технология Active не предоставляет серверу возможность подключения к главному циклу обработки сообщений контейнера. MFC требуется доступ к циклу обработки сообщений приложения-контейнера, чтобы обрабатывать сочетания клавиш и обработку времени простоя.

Если вы создаете сервер автоматизации и сервер не имеет пользовательского интерфейса, сервер можно сделать внутрипроцессным сервером и полностью разместить его в библиотеке DLL.

## <a name="what-do-you-want-to-know-more-about"></a>Дополнительные сведения

- [Серверы автоматизации](../mfc/automation-servers.md)

## <a name="see-also"></a>См. также

[Создание библиотек DLL C/C++ в Visual Studio](dlls-in-visual-cpp.md)
