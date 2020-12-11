---
description: 'Дополнительные сведения: использование строк настраиваемого формата в элементе управления средства выбора даты и времени'
title: Использование строк пользовательского формата в элементе выбора даты и времени
ms.date: 11/04/2016
helpviewer_keywords:
- CDateTimeCtrl class [MFC], display styles
- DateTimePicker control [MFC], display styles
- DateTimePicker control [MFC]
ms.assetid: 7d577f03-6ca0-4597-9093-50b78f304719
ms.openlocfilehash: 91add199ffd852a107588617d47a2fd51136596d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97154556"
---
# <a name="using-custom-format-strings-in-a-date-and-time-picker-control"></a>Использование строк пользовательского формата в элементе выбора даты и времени

По умолчанию элементы управления выбор даты и времени предоставляют три типа форматов (каждый формат, соответствующий уникальному стилю) для отображения текущей даты или времени:

- **DTS_LONGDATEFORMAT** Отображает дату в длинном формате, создавая выходные данные, например "Среда, 3 января, 2000".

- **DTS_SHORTDATEFORMAT** Отображает дату в кратком формате, выдавая выходные данные, например "1/3/00".

- **DTS_TIMEFORMAT** Отображает время в длинном формате, создавая выходные данные, например "5:31:42 PM".

Однако можно настроить внешний вид даты или времени с помощью строки настраиваемого формата. Эта пользовательская строка состоит из либо существующих символов формата, неформатированных символов, либо их комбинации. После сборки пользовательской строки выполните вызов [CDateTimeCtrl:: сетформат](../mfc/reference/cdatetimectrl-class.md#setformat) , передав пользовательскую строку. Затем элемент управления "Выбор даты и времени" отобразит текущее значение с помощью строки настраиваемого формата.

В следующем примере кода (где *m_dtPicker* является `CDateTimeCtrl` объектом) показано одно возможное решение:

[!code-cpp[NVC_MFCControlLadenDialog#7](../mfc/codesnippet/cpp/using-custom-format-strings-in-a-date-and-time-picker-control_1.cpp)]

Помимо строк настраиваемого формата, элементы управления "Выбор даты и времени" также поддерживают [поля обратного вызова](../mfc/using-callback-fields-in-a-date-and-time-picker-control.md).

## <a name="see-also"></a>См. также раздел

[Использование CDateTimeCtrl](../mfc/using-cdatetimectrl.md)<br/>
[Элементы управления](../mfc/controls-mfc.md)
