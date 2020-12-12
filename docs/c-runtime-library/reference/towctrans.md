---
description: 'Дополнительные сведения о: towctrans'
title: towctrans
ms.date: 11/04/2016
api_name:
- towctrans
api_location:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-string-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- towctrans
helpviewer_keywords:
- towctrans function
ms.assetid: 1ed1e70d-7b31-490f-a7d9-42564b5924ca
ms.openlocfilehash: 7b8ecdd38ca45eb658d5e9f61bf05549878228bd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97318303"
---
# <a name="towctrans"></a>towctrans

Преобразует символ.

## <a name="syntax"></a>Синтаксис

```C
wint_t towctrans(
   wint_t c,
   wctrans_t category
);
```

### <a name="parameters"></a>Параметры

*c*<br/>
Символ, который требуется преобразовать.

*category*<br/>
Идентификатор, который содержит возвращаемое значение [wctrans](wctrans.md).

## <a name="return-value"></a>Возвращаемое значение

Символ *c* после **towctrans** использовал правило преобразования в *категории*.

## <a name="remarks"></a>Комментарии

Значение *Category* должно быть возвращено предыдущим успешным вызовом [wctrans](wctrans.md).

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|**towctrans**|\<wctype.h>|

Дополнительные сведения о совместимости см. в статье [Compatibility](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Пример

Пример, в котором используется **towctrans**, см. в разделе **wctrans** .

## <a name="see-also"></a>См. также раздел

[Преобразование данных](../../c-runtime-library/data-conversion.md)<br/>
