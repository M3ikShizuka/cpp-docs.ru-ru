---
description: 'Дополнительные сведения о: исинф'
title: isinf
ms.date: 01/31/2019
f1_keywords:
- isinf
- math/isinf
helpviewer_keywords:
- isinf function
ms.openlocfilehash: f174855ddbb8cc43fd7338d4254c0f03bf53967d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332641"
---
# <a name="isinf"></a>isinf

Определяет, является ли значение с плавающей запятой бесконечным.

## <a name="syntax"></a>Синтаксис

```C
int isinf(
   /* floating-point */ x
); /* C-only macro */

template <class FloatingType>
inline bool isinf(
   FloatingType x
) throw(); /* C++-only template function */
```

### <a name="parameters"></a>Параметры

*x*<br/>
Проверяемое значение с плавающей запятой.

## <a name="return-value"></a>Возвращаемое значение

**исинф** возвращает ненулевое значение ( **`true`** в коде C++), если аргумент *x* является положительной или отрицательной бесконечностью. **исинф** возвращает 0 ( **`false`** в коде C++), если аргумент является конечным или нечисловым. Как обычные, так и поднормальные значения с плавающей запятой считаются конечными.

## <a name="remarks"></a>Комментарии

**исинф** — это макрос, скомпилированный как C, и встроенная функция шаблона при компиляции в виде C++.

## <a name="requirements"></a>Требования

|Функция|Обязательный заголовок (C)|Обязательный заголовок (C++)|
|--------------|---------------------------|-------------------------------|
|**исинф**|\<math.h>|\<math.h> или \<cmath>|

Дополнительные сведения о совместимости см. в разделе [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="see-also"></a>См. также раздел

[Поддержка операций с плавающей запятой](../../c-runtime-library/floating-point-support.md)<br/>
[fpclassify](fpclassify.md)<br/>
[_fpclass, _fpclassf](fpclass-fpclassf.md)<br/>
[isfinite, _finite, _finitef](finite-finitef.md)<br/>
[isnan, _isnan, _isnanf](isnan-isnan-isnanf.md)<br/>
[isnormal](isnormal.md)<br/>
