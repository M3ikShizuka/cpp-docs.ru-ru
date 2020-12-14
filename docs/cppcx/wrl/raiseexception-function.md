---
description: Дополнительные сведения о функции RaiseException
title: RaiseException - функция
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- internal/Microsoft::WRL::Details::RaiseException
helpviewer_keywords:
- RaiseException function
ms.assetid: f9c74f6d-112a-4d2e-900f-622f795d5dbf
ms.openlocfilehash: b5353757ff04ab12c0fc61da6b2e98b2df835ef0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97198444"
---
# <a name="raiseexception-function"></a>RaiseException - функция

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
inline void __declspec(noreturn)   RaiseException(
      HRESULT hr,
      DWORD dwExceptionFlags = EXCEPTION_NONCONTINUABLE);
```

### <a name="parameters"></a>Параметры

*ч*<br/>
Код исключения вызванного исключения; то есть значение HRESULT невыполненной операции.

*двексцептионфлагс*<br/>
Флаг, указывающий на непрерывное исключение (значение флага равно нулю) или непостоянное исключение (значение флага не равно нулю). По умолчанию исключение недоступно.

## <a name="remarks"></a>Комментарии

Вызывает исключение в вызывающем потоке.

Дополнительные сведения см. в описании `RaiseException` функции Windows.

## <a name="requirements"></a>Требования

**Заголовок:** internal. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL::D состояния](microsoft-wrl-details-namespace.md)
