---
description: 'Дополнительные сведения о методе Platform:: ReCreateException'
title: 'Метод Platform:: RecreateException'
ms.date: 12/30/2016
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::Exception
helpviewer_keywords:
- Platform::Exception Class
ms.assetid: fa73d1ab-86e4-4d26-a7d9-81938c1c7e77
ms.openlocfilehash: 273f60055e4cf5a940558ba5dcaa4aa6a7c70bca
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97308059"
---
# <a name="platformrecreateexception-method"></a>Метод Platform::ReCreateException

Этот метод предназначен только для внутреннего использования и не предназначен для пользовательского кода. Вместо него используйте метод Exception::CreateException.

## <a name="syntax"></a>Синтаксис

```cpp
static Exception^ ReCreateException(int hr)
```

### <a name="parameters"></a>Параметры

*ч*

### <a name="property-valuereturn-value"></a>Значение свойства/возвращаемое значение

Возвращает новый Platform::Exception^, основываясь на указанном значении HRESULT.
