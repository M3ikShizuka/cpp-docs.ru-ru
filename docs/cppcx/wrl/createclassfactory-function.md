---
description: Дополнительные сведения о функции Createclassfactory-
title: CreateClassFactory - функция
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Details::CreateClassFactory
helpviewer_keywords:
- CreateClassFactory function
ms.assetid: 772d5d1b-8872-4745-81ca-521a39564713
ms.openlocfilehash: 99565ee732843f57426f10375ffabc7680ef3c62
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97273063"
---
# <a name="createclassfactory-function"></a>CreateClassFactory - функция

Создает фабрику, которая создает экземпляры указанного класса.

## <a name="syntax"></a>Синтаксис

```cpp
template<typename Factory>
inline HRESULT STDMETHODCALLTYPE CreateClassFactory(
   _In_ unsigned int *flags,
   _In_ const CreatorMap* entry,
   REFIID riid,
   _Outptr_ IUnknown **ppFactory
) throw();
```

### <a name="parameters"></a>Параметры

*flags*<br/>
Сочетание одного или нескольких значений перечисления [RuntimeClassType](runtimeclasstype-enumeration.md) .

*операции*<br/>
Указатель на [CreatorMap](creatormap-structure.md) , содержащий сведения об инициализации и регистрации параметра *riid*.

*riid*<br/>
Ссылка на идентификатор интерфейса.

*ппфактори*<br/>
Если эта операция завершается успешно, указатель на фабрику класса.

## <a name="return-value"></a>Возвращаемое значение

Значение S_OK, если операция завершилась успешно; в противном случае — значение HRESULT, указывающее на ошибку.

## <a name="remarks"></a>Комментарии

Если *фабрика* параметров шаблона не является производной от интерфейса, генерируется ошибка Assert `IClassFactory` .

## <a name="requirements"></a>Требования

**Заголовок:** Module. h

**Пространство имен:** Microsoft::WRL

## <a name="see-also"></a>См. также раздел

[Microsoft:: WRL:: оболочки::D пространство имен состояния](microsoft-wrl-wrappers-details-namespace.md)
