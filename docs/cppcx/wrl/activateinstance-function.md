---
description: Дополнительные сведения о функции ActivateInstance
title: ActivateInstance - функция
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- client/Windows::Foundation::ActivateInstance
- client/ABI::Windows::Foundation::ActivateInstance
helpviewer_keywords:
- ActivateInstance function
ms.assetid: 8cfd1dd9-5fda-4cc2-acf8-d40e783b3875
ms.openlocfilehash: 03d7b67810ee2ab287072546b098f81f43687233
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97287857"
---
# <a name="activateinstance-function"></a>ActivateInstance - функция

Регистрирует и извлекает экземпляр указанного типа, определенного в указанном ИДЕНТИФИКАТОРе класса.

## <a name="syntax"></a>Синтаксис

```cpp
template<typename T>
inline HRESULT ActivateInstance(
   _In_ HSTRING activatableClassId,
   _Out_ Microsoft::WRL::Details::ComPtrRef<T> instance
);
```

### <a name="parameters"></a>Параметры

*T*<br/>
Тип для активации.

*Запись*<br/>
Имя идентификатора класса, определяющего параметр *T*.

*вхождение*<br/>
По завершении этой операции ссылка на экземпляр *T*.

## <a name="return-value"></a>Возвращаемое значение

S_OK в случае успеха; в противном случае возвращается ошибка HRESULT, указывающая причину ошибки.

## <a name="requirements"></a>Требования

**Заголовок:** client.h

**Пространство имен:** Windows:: Foundation

## <a name="see-also"></a>См. также раздел

[Пространство имен Windows:: Foundation](windows-foundation-namespace.md)
