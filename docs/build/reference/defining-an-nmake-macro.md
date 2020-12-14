---
description: 'Дополнительные сведения: определение макроса NMAKE'
title: Определение макроса NMAKE
ms.date: 11/04/2016
helpviewer_keywords:
- macros, NMAKE
- defining NMAKE macros
- NMAKE macros, defining
ms.assetid: 45aae451-9d33-4a3d-8799-2e0cae17070d
ms.openlocfilehash: 133e05cac2a236a38f6b2d1e719f1b66fd73760d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97201642"
---
# <a name="defining-an-nmake-macro"></a>Определение макроса NMAKE

## <a name="syntax"></a>Синтаксис

```

macroname=string
```

## <a name="remarks"></a>Remarks

*ИмяМакроса* — это сочетание букв, цифр и знаков подчеркивания (_) до 1 024 символов и чувствительное к регистру. *ИмяМакроса* может содержать вызванный макрос. Если *имяМакроса* полностью состоит из вызванного макроса, то вызываемый макрос не может иметь значение null или быть неопределенным.

`string`Может быть любой последовательностью из нуля или более символов. Пустая строка содержит ноль символов или только пробелы или символы табуляции. `string`Может содержать вызов макроса.

## <a name="what-do-you-want-to-know-more-about"></a>Дополнительные сведения

[Специальные символы в макросах](special-characters-in-macros.md)

[Пустые и неопределенные макросы](null-and-undefined-macros.md)

[Где следует определять макросы](where-to-define-macros.md)

[Приоритет в макроопределениях](precedence-in-macro-definitions.md)

## <a name="see-also"></a>См. также раздел

[Макросы и программа NMAKE](macros-and-nmake.md)
