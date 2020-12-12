---
description: 'Дополнительные сведения о: &lt; ccomplex&gt;'
title: '&lt;ccomplex&gt;'
ms.date: 07/11/2019
f1_keywords:
- <ccomplex>
- ccomplex
helpviewer_keywords:
- ccomplex header
ms.assetid: a9fcb5f0-88e3-464b-a5fd-d1afb8cd7e6f
ms.openlocfilehash: d657d7b0b2a203bcbad93ff1c78f6b78eb4d7707
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97325319"
---
# <a name="ltccomplexgt"></a>&lt;ccomplex&gt;

Включает заголовок стандартной библиотеки C++ [\<complex>](complex.md) .

> [!NOTE]
> Заголовок стандартной библиотеки C \<complex.h> не включается в \<ccomplex> , так как он фактически заменяется перегрузками C++ в \<complex> и \<cmath> . Это делает \<ccomplex> заголовок избыточным. \<complex.h>Заголовок является устаревшим в C++. \<ccomplex>Заголовок является устаревшим в c++ 17 и удаляется в черновом стандарте c++ 20.

## <a name="requirements"></a>Требования

**Заголовок:**\<ccomplex>

**Пространство имен:** std

## <a name="remarks"></a>Комментарии

Имя `clog` , которое объявлено в \<complex.h> , не определено в `std` пространстве имен из-за возможных конфликтов с `clog` , объявленных в [\<iostream>](iostream.md) .

## <a name="see-also"></a>См. также раздел

[\<complex>](complex.md)\
[\<cmath>](cmath.md)\
[Справочник по файлам заголовков](cpp-standard-library-header-files.md)\
[Общие сведения о стандартной библиотеке C++](cpp-standard-library-overview.md)\
[Безопасность потоков в стандартной библиотеке C++](thread-safety-in-the-cpp-standard-library.md)
