---
description: 'Дополнительные сведения: создание класса диалогового окна'
title: Создание классов диалоговых окон
ms.date: 09/06/2019
helpviewer_keywords:
- dialog boxes [MFC], creating
- MFC dialog boxes [MFC], creating
- files [MFC], creating
- dialog classes [MFC], Add Class Wizard
- dialog classes [MFC], creating
ms.assetid: d5321741-da41-47a8-bb1c-6a0e8b28c4c1
ms.openlocfilehash: d135d6acaefbc73f435e48db8f72add7081fdac2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97309450"
---
# <a name="creating-your-dialog-class"></a>Создание классов диалоговых окон

Для каждого диалогового окна в программе создайте новый класс диалогового окна для работы с ресурсом диалогового окна.

[Добавление класса](../ide/adding-a-class-visual-cpp.md) объясняет, как создать новый класс диалогового окна. При создании класса диалогового окна с помощью [мастера классов](reference/mfc-class-wizard.md)он записывает следующие элементы в h-и CPP-файлы, указанные ниже.

В h файл:

- Объявление класса для диалогового класса. Класс является производным от класса [CDialog](reference/cdialog-class.md).

В cpp – файле:

- Схема сообщений для класса.

- Стандартный конструктор для диалогового окна.

- Переопределение функции члена [DoDataExchange](reference/cwnd-class.md#dodataexchange) . Измените эту функцию. Он используется для обмена данными диалоговых окон и проверки, как описано далее в разделе [Обмен и проверка данных диалоговых окон](dialog-data-exchange-and-validation.md).

## <a name="see-also"></a>См. также раздел

[Создание класса диалогового окна с помощью мастеров кода](creating-a-dialog-class-with-code-wizards.md)<br/>
[Работа с диалоговыми окнами в MFC](life-cycle-of-a-dialog-box.md)
