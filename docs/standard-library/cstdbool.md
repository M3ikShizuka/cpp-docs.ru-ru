---
description: 'Дополнительные сведения о: &lt; кстдбул&gt;'
title: '&lt;cstdbool&gt;'
ms.date: 07/11/2019
f1_keywords:
- <cstdbool>
- cstdbool
helpviewer_keywords:
- cstdbool header
ms.assetid: 44ccb8b2-d808-4715-8097-58ba09ab33ed
ms.openlocfilehash: 0711c05ff136f90a701ff707976a172d2bcb1315
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324739"
---
# <a name="ltcstdboolgt"></a>&lt;cstdbool&gt;

Включает заголовок стандартной библиотеки C \<stdbool.h> и добавляет связанные имена в `std` пространство имен.

> [!NOTE]
> Так как \<stdbool.h> заголовок определяет макросы, которые являются ключевыми словами в C++, в том числе он не оказывает никакого влияния. \<stdbool.h>Заголовок является устаревшим в C++. \<cstdbool>Заголовок является устаревшим в c++ 17 и удаляется в черновом стандарте c++ 20.

## <a name="requirements"></a>Требования

**Заголовок:**\<cstdbool>

**Пространство имен:** std

## <a name="remarks"></a>Комментарии

Включение этого заголовка гарантирует, что имена, объявленные с помощью внешней компоновки в заголовке стандартной библиотеки C, объявляются в `std` пространстве имен.

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](cpp-standard-library-header-files.md)\
[Общие сведения о стандартной библиотеке C++](cpp-standard-library-overview.md)\
[Безопасность потоков в стандартной библиотеке C++](thread-safety-in-the-cpp-standard-library.md)
