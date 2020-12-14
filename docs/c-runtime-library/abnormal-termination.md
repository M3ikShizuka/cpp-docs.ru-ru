---
description: 'Дополнительные сведения: _abnormal_termination'
title: _abnormal_termination
ms.date: 11/04/2016
api_name:
- _abnormal_termination
api_location:
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr90.dll
- msvcr120.dll
- msvcrt.dll
- msvcr80.dll
- msvcr100.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- _abnormal_termination
helpviewer_keywords:
- _abnormal_termination
ms.assetid: 952970a4-9586-4c3d-807a-db729448c91c
ms.openlocfilehash: 2fa4b82deeebda7624d8ac96be675efc100ae926
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97224287"
---
# <a name="_abnormal_termination"></a>_abnormal_termination

Указывает, **`__finally`** вошел ли блок [оператора try-finally](../cpp/try-finally-statement.md) , когда система выполняет внутренний список обработчиков завершения.

## <a name="syntax"></a>Синтаксис

```cpp
int   _abnormal_termination(
   );
```

## <a name="return-value"></a>Возвращаемое значение

**`true`** значение, если система *перематывает* стек; в противном случае — **`false`** .

## <a name="remarks"></a>Комментарии

Это внутренняя функция, используемая для управления исключениями очистки, и она не должна вызываться из пользовательского кода.

## <a name="requirements"></a>Требования

|Подпрограмма|Обязательный заголовок|
|-------------|---------------------|
|_abnormal_termination|excpt.h|

## <a name="see-also"></a>См. также

[Оператор try-finally](../cpp/try-finally-statement.md)
