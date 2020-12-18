---
description: 'Подробнее о следующем: Диапазоны чтения'
title: Диапазоны чтения
ms.date: 11/04/2016
ms.assetid: 99de29ce-ab14-46f4-97e1-2081fd996b53
ms.openlocfilehash: afb1ff0f25360de7c47663279bf6f54dd7ca6a48
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97309125"
---
# <a name="reading-ranges"></a>Диапазоны чтения

**ANSI 4.9.6.2** Интерпретация символа дефиса (-), который не является ни первым, ни последним символом в списке сканирования для преобразования % [ в функции `fscanf`

В следующей строке

```
fscanf( fileptr, "%[A-Z]", strptr);
```

считывается любое количество символов в диапазоне A–Z в строке, на которую указывает `strptr`.

## <a name="see-also"></a>См. также

[Функции библиотеки](../c-language/library-functions.md)
