---
description: Дополнительные сведения о:/SWAPRUN
title: /SWAPRUN
ms.date: 11/04/2016
f1_keywords:
- /swaprun_editbin
helpviewer_keywords:
- /SWAPRUN editbin option
- -SWAPRUN editbin option
- SWAPRUN editbin option
ms.assetid: 6eefd7f3-ca47-48e3-8509-323d27cf4ae7
ms.openlocfilehash: 68d53a8d5fa7337fb29f624e26b71790f78d29dd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97230176"
---
# <a name="swaprun"></a>/SWAPRUN

```
/SWAPRUN:{[!]NET|[!]CD}
```

## <a name="remarks"></a>Комментарии

Этот параметр изменяет образ, чтобы операционная система скопировала образ в файл подкачки и запустил его. Используйте этот параметр для образов, которые находятся в сетях или съемных носителях.

Можно добавить или удалить квалификаторы NET или CD.

- Параметр NET указывает, что образ находится в сети.

- CD указывает, что образ находится на компакт-диске или аналогичном съемном носителе.

- Используйте! NET и! CD для отмены эффектов NET и CD.

## <a name="see-also"></a>См. также раздел

[Параметры EDITBIN](editbin-options.md)
