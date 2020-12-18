---
description: 'Подробнее о следующем: Перевод: Диагностика'
title: 'Перевод: Диагностика'
ms.date: 11/04/2016
ms.assetid: 3730ca7c-0147-452d-bd4a-6a1e97e9793e
ms.openlocfilehash: 09fc44dea8d51dbb267d402745c8c2a095b969d8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97243059"
---
# <a name="translation-diagnostics"></a>Перевод: Диагностика

**ANSI 2.1.1.3** Определение диагностики

Microsoft C создает сообщения об ошибках в следующем виде:

> *filename* **(** *line-number* **) :** *diagnostic* **C**<em>number</em> *message*

Где *filename* обозначает имя исходного файла, в котором была обнаружена ошибка; *line-number* — номер строки, в которой компилятор обнаружил ошибку; *diagnostic* имеет значение "error" (ошибка) или "warning" (предупреждение); *number* — уникальное четырехзначное число, определяющее ошибку или предупреждение (с предшествующим символом **C**, как указано в синтаксисе); а *message* — поясняющее сообщение.

## <a name="see-also"></a>См. также

[Поведение, определяемое реализацией](../c-language/implementation-defined-behavior.md)
