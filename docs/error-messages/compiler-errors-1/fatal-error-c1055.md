---
description: 'Дополнительные сведения о: Неустранимая ошибка C1055'
title: Неустранимая ошибка C1055
ms.date: 11/04/2016
f1_keywords:
- C1055
helpviewer_keywords:
- C1055
ms.assetid: a9fb9190-d7eb-4d5f-b1a2-a41e584a28c1
ms.openlocfilehash: f85d3bc19b9dcd2ba3f4338e78c55cc7aa549fb6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97251652"
---
# <a name="fatal-error-c1055"></a>Неустранимая ошибка C1055

ограничение компилятора: недостаточно ключей

Исходный файл содержит слишком много символов. Компилятору не хватило хэш-ключей для таблицы символов.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>Возможные способы устранения этой ошибки

1. Разделите исходный файл на небольшие файлы.

1. Исключите ненужные файлы заголовков.

1. Повторно используйте временные и глобальные переменные вместо создания новых.
