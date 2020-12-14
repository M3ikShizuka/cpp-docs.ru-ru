---
description: Дополнительные сведения о подстановке макросов
title: Макроподстановка
ms.date: 11/04/2016
helpviewer_keywords:
- NMAKE program, macro substitution
- macros, NMAKE
- substitution macros in NMAKE
ms.assetid: 47465cfe-fd92-49db-aebe-7c2d7ecceb73
ms.openlocfilehash: 5e1531afb210b4671632bca2540bfc7562653139
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97199185"
---
# <a name="macro-substitution"></a>Макроподстановка

При вызове *имяМакроса* каждое вхождение *строка1* в строку определения заменяется строкой *строка2*.

## <a name="syntax"></a>Синтаксис

```
$(macroname:string1=string2)
```

## <a name="remarks"></a>Remarks

Подстановка макросов учитывает регистр и является литералом; *строка1* и *строка2* не могут вызывать макросы. Подстановка не изменяет исходное определение. Текст можно заменить любым предопределенным макросом, кроме [$$@](filename-macros.md) .

Пробелы и символы табуляции не предшествуют двоеточию; все после двоеточия интерпретируется как литерал. Если *строка2* имеет значение null, все вхождения *строка1* удаляются из строки определения макроса.

## <a name="see-also"></a>См. также раздел

[Использование макроса NMAKE](using-an-nmake-macro.md)
