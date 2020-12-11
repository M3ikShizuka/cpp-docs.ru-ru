---
description: 'Дополнительные сведения: TZNAME_MAX'
title: TZNAME_MAX
ms.date: 10/22/2018
f1_keywords:
- TZNAME_MAX
helpviewer_keywords:
- TZNAME_MAX constant
ms.assetid: e2286cb8-751d-4557-9650-5c4b98a8f7be
ms.openlocfilehash: 1c426c82bd198998169c385366ae5188cabd02d8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97162166"
---
# <a name="tzname_max"></a>TZNAME_MAX

**Устарел**. Максимально допустимая длина строки переменной названия часового пояса. Этот макрос был определен в \<limits.h> Visual Studio 2012 и более ранних версиях. Он не определен в Visual Studio 2013 и более поздних версий. Для получения длины, требуемой для хранения имени текущего часового пояса, используйте [_get_tzname](../c-runtime-library/reference/get-tzname.md).

## <a name="syntax"></a>Синтаксис

```
#include <limits.h>
```

## <a name="see-also"></a>См. также раздел

[Константы среды](../c-runtime-library/environmental-constants.md)<br/>
[Глобальные константы](../c-runtime-library/global-constants.md)<br/>
[_get_tzname](../c-runtime-library/reference/get-tzname.md)
