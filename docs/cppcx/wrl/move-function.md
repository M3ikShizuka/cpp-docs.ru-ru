---
description: Дополнительные сведения о функции Move
title: Move - функция
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- internal/Microsoft::WRL::Details::Move
helpviewer_keywords:
- Move function
ms.assetid: c9525426-97e8-4d8c-9877-b689d8a0dc67
ms.openlocfilehash: eada3cac16abc445a9c48d01240f4ccf46d78372
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97209312"
---
# <a name="move-function"></a>Move - функция

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
template<class T>
inline typename RemoveReference<T>::Type&& Move(
   _Inout_ T&& arg
);
```

### <a name="parameters"></a>Параметры

*T*<br/>
Тип аргумента.

*АРГ*<br/>
Аргумент для перемещения.

## <a name="return-value"></a>Возвращаемое значение

Параметр *arg* после удаления ссылки или ссылочного значения rvalue, если таковые имеются, были удалены.

## <a name="remarks"></a>Комментарии

Перемещает указанный аргумент из одного расположения в другое.

Дополнительные сведения см. в разделе **семантика перемещения** в [деклараторе ссылки rvalue:  &&](../../cpp/rvalue-reference-declarator-amp-amp.md).

## <a name="requirements"></a>Требования

**Заголовок:** internal. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="see-also"></a>См. также раздел

[Пространство имен Microsoft:: WRL::D состояния](microsoft-wrl-details-namespace.md)
