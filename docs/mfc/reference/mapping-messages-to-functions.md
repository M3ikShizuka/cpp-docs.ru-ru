---
description: 'Дополнительные сведения: сопоставление сообщений с функциями'
title: Сопоставление сообщений с функциями
ms.date: 09/06/2019
f1_keywords:
- vc.codewiz.mapping.msg.function
helpviewer_keywords:
- Windows messages [MFC], adding message handlers
- message maps [MFC], mapping messages to functions
ms.assetid: a7727a62-f638-4b20-b7f5-131f47200d6a
ms.openlocfilehash: 5bb3decdcc6751c47644acf5f5bff942efe8c725
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97219412"
---
# <a name="mapping-messages-to-functions"></a>Сопоставление сообщений с функциями

[Мастер классов](mfc-class-wizard.md) позволяет привязывать обработчики сообщений (функции-члены классов пользовательских интерфейсов MFC) к сообщениям, создаваемым ресурсами приложения. Для создания привязки используются [схемы сообщений MFC](../../mfc/messages-and-commands-in-the-framework.md) .

При использовании представление классов для создания нового класса, производного от одного из классов платформы, он автоматически помещает полный и функциональный класс в указанные файлы заголовков (. h) и реализации (. cpp).

> [!NOTE]
> Чтобы добавить новый класс, который не обрабатывает сообщения, создайте класс непосредственно в текстовом редакторе.

### <a name="to-define-or-remove-a-message-handler-using-the-class-wizard"></a>Определение или удаление обработчика сообщений с помощью мастера классов

1. В **представление классов** щелкните правой кнопкой мыши класс.

1. В контекстном меню выберите пункт [мастер классов](mfc-class-wizard.md).

## <a name="see-also"></a>См. также раздел

[Обработчик сообщений MFC](../../mfc/reference/adding-an-mfc-message-handler.md)<br/>
[Добавление функциональных возможностей с помощью мастеров кода](../../ide/adding-functionality-with-code-wizards-cpp.md)<br/>
[Добавление класса](../../ide/adding-a-class-visual-cpp.md)<br/>
[Добавление функции-члена](../../ide/adding-a-member-function-visual-cpp.md)<br/>
[Добавление переменной-члена](../../ide/adding-a-member-variable-visual-cpp.md)<br/>
[Переопределение виртуальной функции](../../ide/overriding-a-virtual-function-visual-cpp.md)<br/>
[Перемещение по структуре класса](../../ide/navigate-code-cpp.md)
