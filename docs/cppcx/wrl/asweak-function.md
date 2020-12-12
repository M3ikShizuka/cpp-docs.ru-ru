---
description: Дополнительные сведения о функции AsWeak
title: AsWeak - функция
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- client/Microsoft::WRL::AsWeak
helpviewer_keywords:
- AsWeak function
ms.assetid: a6f10cfc-c1d6-4761-adb9-1a119cc99913
ms.openlocfilehash: a02776f06aab4d7505b38fbb1120c36a82e97368
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97175850"
---
# <a name="asweak-function"></a>AsWeak - функция

Извлекает слабую ссылку на определенный экземпляр.

## <a name="syntax"></a>Синтаксис

```cpp
template<typename T>
HRESULT AsWeak(
   _In_ T* p,
   _Out_ WeakRef* pWeak
);
```

### <a name="parameters"></a>Параметры

*T*<br/>
Указатель на тип параметра *p*.

*p*<br/>
Экземпляр типа.

*пвеак*<br/>
По завершении этой операции указатель на слабую ссылку на параметр *p*.

## <a name="return-value"></a>Возвращаемое значение

S_OK, если эта операция выполнена успешно; в противном случае возвращается ошибка HRESULT, указывающая причину сбоя.

## <a name="requirements"></a>Требования

**Заголовок:** client.h

**Пространство имен:** Microsoft::WRL

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL](microsoft-wrl-namespace.md)
