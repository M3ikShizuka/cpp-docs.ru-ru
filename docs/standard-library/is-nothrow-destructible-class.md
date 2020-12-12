---
description: 'Дополнительные сведения о: is_nothrow_destructible классе'
title: Класс is_nothrow_destructible
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_nothrow_destructible
helpviewer_keywords:
- is_nothrow_destructible
ms.assetid: 0bbd8a28-e312-4d72-bd28-aac027f974d3
ms.openlocfilehash: 017cc6de7ce5c618fcc3f47540efd34b5fdc40a4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323622"
---
# <a name="is_nothrow_destructible-class"></a>Класс is_nothrow_destructible

Проверяет, является ли тип уничтожаемым и знает ли компилятор, что деструктор не выдает исключения.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
struct is_nothrow_destructible;
```

### <a name="parameters"></a>Параметры

*T*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *T* является типом можно уничтожить, и деструктор известен компилятору, не вызываемому. В противном случае — значение false.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
