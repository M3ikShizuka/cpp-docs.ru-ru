---
description: 'Подробнее о следующем: Диагностика, напечатанная функцией assert'
title: Диагностика, напечатанная функцией assert
ms.date: 11/04/2016
ms.assetid: 78b64200-520d-40da-9a61-71553f411d4f
ms.openlocfilehash: cab4f6dfd2cab7d4b46486a103b39abb6ca17005
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97186796"
---
# <a name="diagnostic-printed-by-the-assert-function"></a>Диагностика, напечатанная функцией assert

**ANSI 4.2** Диагностика, выведенная функцией assert, и поведение завершения функции **assert**

Функция **assert** выводит диагностическое сообщение и вызывает подпрограмму **abort**, если значение выражения — false (0). Диагностическое сообщение имеет форму

> **Сбой утверждения**: <em>expression</em> **, file** <em>filename</em> **, line** *linenumber*

где *filename* — это имя исходного файла, а *linenumber* — номер строки утверждения, завершившегося сбоем в файле исходного кода. Если *expression* равно true (ненулевое), никакие действия не предпринимаются.

## <a name="see-also"></a>См. также

[Функции библиотеки](../c-language/library-functions.md)
