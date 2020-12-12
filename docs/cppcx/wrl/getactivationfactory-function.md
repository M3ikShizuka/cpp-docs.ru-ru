---
description: Дополнительные сведения о функции GetActivationFactory
title: GetActivationFactory - функция
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Details::GetActivationFactory
- client/ABI::Windows::Foundation::GetActivationFactory
- client/Windows::Foundation::GetActivationFactory
helpviewer_keywords:
- GetActivationFactory function
ms.assetid: 5736d285-6beb-42aa-8788-e261c0010afe
ms.openlocfilehash: ae2384e0620282723c6f10090a0028347408b271
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97124635"
---
# <a name="getactivationfactory-function"></a>GetActivationFactory - функция

Извлекает фабрику активации для типа, указанного в параметре шаблона.

## <a name="syntax"></a>Синтаксис

```cpp
template<typename T>
inline HRESULT GetActivationFactory(
   _In_ HSTRING activatableClassId,
   _Out_ Microsoft::WRL::Details::ComPtrRef<T> factory
);
```

### <a name="parameters"></a>Параметры

*T*<br/>
Параметр шаблона, который определяет тип фабрики активации.

*Запись*<br/>
Имя класса, который может создать фабрика активации.

*фабрика*<br/>
По завершении этой операции — ссылка на фабрику активации для типа *T*.

## <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, указывающее причину неудачного завершения операции.

## <a name="requirements"></a>Требования

**Заголовок:** client.h

**Пространство имен:** Windows:: Foundation

## <a name="see-also"></a>См. также раздел

[Пространство имен Windows:: Foundation](windows-foundation-namespace.md)
