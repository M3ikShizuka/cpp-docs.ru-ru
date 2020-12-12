---
description: 'Дополнительные сведения: ограничения для полей пути'
title: Пределы поля "Путь"
ms.date: 11/04/2016
f1_keywords:
- _MAX_EXT
- _MAX_DIR
- _MAX_PATH
- _MAX_FNAME
- _MAX_DRIVE
helpviewer_keywords:
- path field constants
- MAX_FNAME constant
- _MAX_DIR constant
- _MAX_DRIVE constant
- paths, maximum limit
- _MAX_PATH constant
- MAX_DRIVE constant
- _MAX_FNAME constant
- _MAX_EXT constant
- MAX_DIR constant
- MAX_EXT constant
ms.assetid: 2b5d0e43-1347-45b4-8397-24a8a45c444e
ms.openlocfilehash: 41698d946e45a78f9b89f40fdd3c7c58af5d4354
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97213485"
---
# <a name="path-field-limits"></a>Пределы поля "Путь"

## <a name="syntax"></a>Синтаксис

```cpp
#include <stdlib.h>
```

## <a name="remarks"></a>Remarks

Эти константы определяют максимальную длину пути и отдельных полей в пути.

|Константа|Значение|
|--------------|-------------|
|`_MAX_DIR`|Максимальная длина компонента каталога|
|`_MAX_DRIVE`|Максимальная длина компонента диска|
|`_MAX_EXT`|Максимальная длина компонента расширения|
|`_MAX_FNAME`|Максимальная длина компонента имени файла|
|`_MAX_PATH`|Максимальная длина полного пути|

> [!NOTE]
> Среда выполнения языка C поддерживает длину пути до 32768 символов, но поддержка таких длинных путей зависит от операционной системы, а именно, от файловой системы. Для полной обратной совместимости с файловыми системами FAT32 общая длина полей не должна превышать `_MAX_PATH`. Файловая система Windows NTFS поддерживает пути длиной до 32 768 символов, но только при использовании API Юникода. Если вы используете длинные пути, указывайте в начале пути символы \\\\?\ и используйте версии для Юникода функций среды выполнения языка С.

## <a name="see-also"></a>См. также раздел

[Глобальные константы](../c-runtime-library/global-constants.md)
