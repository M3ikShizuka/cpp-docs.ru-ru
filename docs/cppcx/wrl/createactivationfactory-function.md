---
description: Дополнительные сведения о функции Креатеактиватионфактори
title: CreateActivationFactory - функция
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Details::CreateActivationFactory
helpviewer_keywords:
- CreateActivationFactory function
ms.assetid: a1a53e04-6757-4faf-a4c8-ecf06e43b959
ms.openlocfilehash: 25f2181a00bb018361b05ea6570ebbadc6f7a975
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97273113"
---
# <a name="createactivationfactory-function"></a>CreateActivationFactory - функция

Создает фабрику, производящую экземпляры указанного класса, которые могут быть активированы средой выполнения Windows.

## <a name="syntax"></a>Синтаксис

```cpp
template<typename Factory>
   inline HRESULT STDMETHODCALLTYPE CreateActivationFactory(
      _In_ unsigned int *flags,        _In_ const CreatorMap* entry,
      REFIID riid,
   _Outptr_ IUnknown **ppFactory) throw();
```

### <a name="parameters"></a>Параметры

*flags*<br/>
Сочетание одного или нескольких значений перечисления [RuntimeClassType](runtimeclasstype-enumeration.md) .

*операции*<br/>
Указатель на [CreatorMap](creatormap-structure.md) , содержащий сведения об инициализации и регистрации параметра *riid*.

*riid*<br/>
Ссылка на идентификатор интерфейса.

*ппфактори*<br/>
Если эта операция завершается успешно, указатель на фабрику активации.

## <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, указывающее на ошибку.

## <a name="remarks"></a>Комментарии

Если *фабрика* параметров шаблона не является производной от интерфейса, генерируется ошибка Assert `IActivationFactory` .

## <a name="requirements"></a>Требования

**Заголовок:** Module. h

**Пространство имен:** Microsoft::WRL

## <a name="see-also"></a>См. также раздел

[Microsoft:: WRL:: оболочки::D пространство имен состояния](microsoft-wrl-wrappers-details-namespace.md)
