---
description: 'Дополнительные сведения о: &lt; ctgmath&gt;'
title: '&lt;ctgmath&gt;'
ms.date: 07/11/2019
f1_keywords:
- <ctgmath>
helpviewer_keywords:
- ctgmath header
ms.assetid: ff521893-f445-4dc8-a2f6-699185bb7024
ms.openlocfilehash: 1968422bc32695eb15cff69c53fcaadf63ac5c14
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98126589"
---
# <a name="ltctgmathgt"></a>&lt;ctgmath&gt;

Фактически включает заголовки стандартной библиотеки C++ \<complex> и \<cmath> , которые предоставляют математические макросы с универсальными типами, эквивалентные \<tgmath.h> .

> [!NOTE]
> Заголовок стандартной библиотеки C \<tgmath.h> не включается в \<ctgmath> , так как он фактически заменяется перегрузками C++ в \<complex> и \<cmath> . Это делает \<ctgmath> заголовок избыточным. \<tgmath.h>Заголовок является устаревшим в C++. \<ctgmath>Заголовок является устаревшим в c++ 17 и удаляется в черновом стандарте c++ 20.

## <a name="requirements"></a>Требования

**Заголовок:**\<ctgmath>

**Пространство имен:** std

## <a name="remarks"></a>Remarks

Функциональные возможности заголовка стандартной библиотеки C \<tgmath.h> предоставляются перегрузками в \<complex> и \<cmath> .

## <a name="see-also"></a>См. также раздел

[\<complex>](complex.md)\
[\<cmath>](cmath.md)\
[Справочник по файлам заголовков](cpp-standard-library-header-files.md)\
[Общие сведения о стандартной библиотеке C++](cpp-standard-library-overview.md)\
[Безопасность потоков в стандартной библиотеке C++](thread-safety-in-the-cpp-standard-library.md)
