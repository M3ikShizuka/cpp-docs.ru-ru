---
description: 'Дополнительные сведения о: &lt; ctgmath&gt;'
title: '&lt;ctgmath&gt;'
ms.date: 07/11/2019
f1_keywords:
- <ctgmath>
- ctgmath
helpviewer_keywords:
- ctgmath header
ms.assetid: ff521893-f445-4dc8-a2f6-699185bb7024
ms.openlocfilehash: f1033a944699f4c124114c49e0e30f8b30804a1e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97324699"
---
# <a name="ltctgmathgt"></a>&lt;ctgmath&gt;

Фактически включает заголовки стандартной библиотеки C++ \<complex> и \<cmath> , которые предоставляют математические макросы с универсальными типами, эквивалентные \<tgmath.h> .

> [!NOTE]
> Заголовок стандартной библиотеки C \<tgmath.h> не включается в \<ctgmath> , так как он фактически заменяется перегрузками C++ в \<complex> и \<cmath> . Это делает \<ctgmath> заголовок избыточным. \<tgmath.h>Заголовок является устаревшим в C++. \<ctgmath>Заголовок является устаревшим в c++ 17 и удаляется в черновом стандарте c++ 20.

## <a name="requirements"></a>Требования

**Заголовок:**\<ctgmath>

**Пространство имен:** std

## <a name="remarks"></a>Комментарии

Функциональные возможности заголовка стандартной библиотеки C \<tgmath.h> предоставляются перегрузками в \<complex> и \<cmath> .

## <a name="see-also"></a>См. также раздел

[\<complex>](complex.md)\
[\<cmath>](cmath.md)\
[Справочник по файлам заголовков](cpp-standard-library-header-files.md)\
[Общие сведения о стандартной библиотеке C++](cpp-standard-library-overview.md)\
[Безопасность потоков в стандартной библиотеке C++](thread-safety-in-the-cpp-standard-library.md)
