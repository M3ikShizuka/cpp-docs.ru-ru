---
description: Дополнительные сведения о функции Активатионфакторикаллбакк
title: ActivationFactoryCallback - функция
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Details::ActivationFactoryCallback
helpviewer_keywords:
- ActivationFactoryCallback function
ms.assetid: dd40c79b-1273-4f2a-8c24-ae9926fb4fd9
ms.openlocfilehash: 9398b3f681e32c7a73b46de549ce7c41a3af6196
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97204619"
---
# <a name="activationfactorycallback-function"></a>ActivationFactoryCallback - функция

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
inline HRESULT STDAPICALLTYPE ActivationFactoryCallback(
   HSTRING activationId,
   IActivationFactory **ppFactory
);
```

### <a name="parameters"></a>Параметры

*activationId*<br/>
Обрабатывает строку, указывающую имя класса среды выполнения.

*ппфактори*<br/>
По завершении этой операции фабрика активации, соответствующая параметру *ActivationID*.

## <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, описывающее тип сбоя. Вероятные ошибки HRESULT — это CLASS_E_CLASSNOTAVAILABLE и E_INVALIDARG.

## <a name="remarks"></a>Комментарии

Возвращает фабрику активации для указанного идентификатора активации.

Среда выполнения Windows вызывает эту функцию обратного вызова для запроса объекта, указанного именем класса среды выполнения.

## <a name="requirements"></a>Требования

**Заголовок:** Module. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL::D состояния](microsoft-wrl-details-namespace.md)
