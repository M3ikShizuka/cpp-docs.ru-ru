---
description: 'Дополнительные сведения о: BSCMAKE Warning BK4504'
title: Предупреждение BSCMAKE BK4504
ms.date: 11/04/2016
f1_keywords:
- BK4504
helpviewer_keywords:
- BK4504
ms.assetid: b56ee2d4-ad44-40f4-98c0-75934ea44a6c
ms.openlocfilehash: 8b07c15b03a040ea19ec368c6f869d02f3e36f79
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97237833"
---
# <a name="bscmake-warning-bk4504"></a>Предупреждение BSCMAKE BK4504

файл содержит слишком много ссылок; пропуск дальнейших ссылок из этого источника

Файл. cpp содержит более 64 000 ссылок на символы. Когда BSCMAKE обнаружил 64 000 ссылок в файле, он игнорирует все дальнейшие ссылки.

Чтобы устранить проблему, Разделите файл на два или более файлов, каждый из которых содержит менее 64 000 ссылок на символы, или используйте `#pragma component(browser)` директиву препроцессора для ограничения символов, создаваемых для определенных ссылок. Дополнительные сведения см. в разделе [Component](../../preprocessor/component.md).
