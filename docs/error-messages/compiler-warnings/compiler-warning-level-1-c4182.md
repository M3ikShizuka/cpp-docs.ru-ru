---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 1) C4182'
title: Предупреждение компилятора (уровень 1) C4182
ms.date: 11/04/2016
f1_keywords:
- C4182
helpviewer_keywords:
- C4182
ms.assetid: 8970f3c6-e2dd-407e-b2ec-964360eb8b43
ms.openlocfilehash: 975d3ceea5e2b7504fda5c7d33e88b52cda9e572
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97266706"
---
# <a name="compiler-warning-level-1-c4182"></a>Предупреждение компилятора (уровень 1) C4182

\#включить уровень вложенности "число"; Возможна бесконечная рекурсия

Компилятору недостаточно места в куче из-за количества вложенных файлов include. Файл include является вложенным, когда он включается из другого файла include.

Это сообщение является информационным и предшествует ошибке [C1076](../../error-messages/compiler-errors-1/fatal-error-c1076.md).
