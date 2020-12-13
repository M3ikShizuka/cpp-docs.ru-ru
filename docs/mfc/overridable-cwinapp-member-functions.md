---
description: Дополнительные сведения о переопределяемых функциях — членах CWinApp
title: Переопределяемые функции-члены CWinApp
ms.date: 11/04/2016
helpviewer_keywords:
- overriding [MFC], overridable functions in CWinApp
- application class [MFC]
- CWinApp class [MFC], overridables
ms.assetid: 07183d5e-734b-45d9-a8b6-9dde4adac0b4
ms.openlocfilehash: 3958ad0edc1fbdb77e1f6ce3252fd03d7595344a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330106"
---
# <a name="overridable-cwinapp-member-functions"></a>Переопределяемые функции-члены CWinApp

[CWinApp](reference/cwinapp-class.md) предоставляет несколько ключевых функций-членов, допускающих `CWinApp` Переопределение (переопределяет эти члены из класса [CWinThread](reference/cwinthread-class.md), от которого `CWinApp` наследуется):

- [InitInstance](initinstance-member-function.md)

- [Выполнить](run-member-function.md)

- [ExitInstance](exitinstance-member-function.md)

- [Обработчик](onidle-member-function.md)

Единственной `CWinApp` функцией-членом, которую необходимо переопределить, является `InitInstance` .

## <a name="see-also"></a>См. также раздел

[CWinApp: класс Application](cwinapp-the-application-class.md)
