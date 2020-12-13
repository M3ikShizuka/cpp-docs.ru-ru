---
description: 'Дополнительные сведения о: Неустранимая ошибка C1071'
title: Неустранимая ошибка C1071
ms.date: 11/04/2016
f1_keywords:
- C1071
helpviewer_keywords:
- C1071
ms.assetid: 489f1786-370e-4ecd-af67-538fe6e5bd4e
ms.openlocfilehash: c4a6734dcb515b6d495eac720f83ba39be3c3677
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97344384"
---
# <a name="fatal-error-c1071"></a>Неустранимая ошибка C1071

непредвиденное обнаружение конца файла в комментарии

Компилятор достиг конца файла при сканировании комментария.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>Чтобы устранить ошибку, проверьте указанные ниже возможные причины ее возникновения.

1. Отсутствует признак конца комментария (*/).

1. Отсутствует символ новой строки после комментария в последней строке исходного файла.

Следующий пример приводит к возникновению ошибки C1071:

```cpp
// C1071.cpp
int main() {
}

/* this comment is fine */
/* forgot the closing tag        // C1071
```
