---
description: 'Дополнительные сведения: МАШИНное неустранимое сообщение об ошибке ML A2031'
title: Некритичная ошибка ML A2031
ms.date: 12/17/2019
ms.custom: error-reference
f1_keywords:
- A2031
helpviewer_keywords:
- A2031
ms.assetid: d5b11f58-4a00-42be-9062-8fa8728e6306
ms.openlocfilehash: 8c92b4e3439a4e660c7c128e52bcadc668778189
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97129224"
---
# <a name="ml-nonfatal-error-a2031"></a>Некритичная ошибка ML A2031

**должен быть индексом или базовым регистром**

Была предпринята попытка использовать регистр, который не является базовым или индексным регистром в выражении памяти.

Например, следующие выражения вызывают эту ошибку:

```asm
[ax]
[bl]
```

## <a name="see-also"></a>См. также раздел

[Сообщения об ошибках ML](ml-error-messages.md)
