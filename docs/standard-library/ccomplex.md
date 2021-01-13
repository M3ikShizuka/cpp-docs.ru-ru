---
description: 'Дополнительные сведения о: &lt; ccomplex&gt;'
title: '&lt;ccomplex&gt;'
ms.date: 07/11/2019
f1_keywords:
- <ccomplex>
helpviewer_keywords:
- ccomplex header
ms.assetid: a9fcb5f0-88e3-464b-a5fd-d1afb8cd7e6f
ms.openlocfilehash: 6c9aa717031238681fa04bc20ab6ca93429553ec
ms.sourcegitcommit: 118e4ad82c0f1c9ac120f105d84224e5fe4cef28
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98126680"
---
# <a name="ltccomplexgt"></a>&lt;ccomplex&gt;

Включает заголовок стандартной библиотеки C++ [\<complex>](complex.md) .

> [!NOTE]
> Заголовок стандартной библиотеки C \<complex.h> не включается в \<ccomplex> , так как он фактически заменяется перегрузками C++ в \<complex> и \<cmath> . Это делает \<ccomplex> заголовок избыточным. \<complex.h>Заголовок является устаревшим в C++. \<ccomplex>Заголовок является устаревшим в c++ 17 и удаляется в черновом стандарте c++ 20.

## <a name="requirements"></a>Требования

**Заголовок:**\<ccomplex>

**Пространство имен:** std

## <a name="remarks"></a>Remarks

Имя `clog` , которое объявлено в \<complex.h> , не определено в `std` пространстве имен из-за возможных конфликтов с `clog` , объявленных в [\<iostream>](iostream.md) .

## <a name="see-also"></a>См. также раздел

[\<complex>](complex.md)\
[\<cmath>](cmath.md)\
[Справочник по файлам заголовков](cpp-standard-library-header-files.md)\
[Общие сведения о стандартной библиотеке C++](cpp-standard-library-overview.md)\
[Безопасность потоков в стандартной библиотеке C++](thread-safety-in-the-cpp-standard-library.md)
