---
description: 'Дополнительные сведения о: Ошибка компилятора C3715'
title: Ошибка компилятора C3715
ms.date: 11/04/2016
f1_keywords:
- C3715
helpviewer_keywords:
- C3715
ms.assetid: ee5dce88-ddc4-4bdb-9464-47467ce1674f
ms.openlocfilehash: b64f7039b15363b36f6cc761f834c64dae255f76
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97189461"
---
# <a name="compiler-error-c3715"></a>Ошибка компилятора C3715

"указатель": должен быть указателем на "class"

Вы указали указатель в [`__hook`](../../cpp/hook.md) или [`__unhook`](../../cpp/unhook.md) , который не указывает на допустимый класс. Чтобы устранить эту ошибку, убедитесь, что **`__hook`** **`__unhook`** вызовы и указывают указатели на допустимые классы.
