---
description: 'Дополнительные сведения о: &lt; кстдбул&gt;'
title: '&lt;cstdbool&gt;'
ms.date: 07/11/2019
f1_keywords:
- <cstdbool>
helpviewer_keywords:
- cstdbool header
ms.assetid: 44ccb8b2-d808-4715-8097-58ba09ab33ed
ms.openlocfilehash: de36d4088c3494cf9b8efcf5175a527da7af8ece
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98126602"
---
# <a name="ltcstdboolgt"></a>&lt;cstdbool&gt;

Включает заголовок стандартной библиотеки C \<stdbool.h> и добавляет связанные имена в `std` пространство имен.

> [!NOTE]
> Так как \<stdbool.h> заголовок определяет макросы, которые являются ключевыми словами в C++, в том числе он не оказывает никакого влияния. \<stdbool.h>Заголовок является устаревшим в C++. \<cstdbool>Заголовок является устаревшим в c++ 17 и удаляется в черновом стандарте c++ 20.

## <a name="requirements"></a>Требования

**Заголовок:**\<cstdbool>

**Пространство имен:** std

## <a name="remarks"></a>Remarks

Включение этого заголовка гарантирует, что имена, объявленные с помощью внешней компоновки в заголовке стандартной библиотеки C, объявляются в `std` пространстве имен.

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](cpp-standard-library-header-files.md)\
[Общие сведения о стандартной библиотеке C++](cpp-standard-library-overview.md)\
[Безопасность потоков в стандартной библиотеке C++](thread-safety-in-the-cpp-standard-library.md)
