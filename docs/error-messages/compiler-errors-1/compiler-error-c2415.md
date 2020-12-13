---
description: 'Дополнительные сведения о: Ошибка компилятора C2415'
title: Ошибка компилятора C2415
ms.date: 11/04/2016
f1_keywords:
- C2415
helpviewer_keywords:
- C2415
ms.assetid: f225c913-2bea-46b1-b096-3d358ac94a15
ms.openlocfilehash: 21bbeabe0a5eacea55d2a38ab515429e6468ba57
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340350"
---
# <a name="compiler-error-c2415"></a>Ошибка компилятора C2415

Недопустимый тип операнда

Код операции не использует операнды этого типа.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>Чтобы устранить ошибку, проверьте указанные ниже возможные причины ее возникновения.

1. Код операции не поддерживает число используемых операндов. Проверьте руководство по языку сборки, чтобы определить правильное число операндов.

1. Новый процессор поддерживает инструкцию с дополнительными типами. Настройте параметр [/Arch (минимальная архитектура ЦП)](../../build/reference/arch-minimum-cpu-architecture.md) , чтобы использовать более поздний процессор.
