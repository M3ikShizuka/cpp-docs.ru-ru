---
description: 'Дополнительные сведения о: Ошибка компилятора C2414'
title: Ошибка компилятора C2414
ms.date: 11/04/2016
f1_keywords:
- C2414
helpviewer_keywords:
- C2414
ms.assetid: bbe94e03-862e-4990-b15e-544ae464727d
ms.openlocfilehash: 5bf2d017ac0018fe092b5a003dee021dd13370b9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97340337"
---
# <a name="compiler-error-c2414"></a>Ошибка компилятора C2414

Недопустимое число операндов

### <a name="to-fix-by-checking-the-following-possible-causes"></a>Чтобы устранить ошибку, проверьте указанные ниже возможные причины ее возникновения.

1. Код операции не поддерживает число используемых операндов. Проверьте руководство по языку сборки, чтобы определить правильное число операндов.

1. Новый процессор поддерживает инструкцию с другим количеством операндов. Настройте параметр [/Arch (минимальная архитектура ЦП)](../../build/reference/arch-minimum-cpu-architecture.md) , чтобы использовать более поздний процессор.
