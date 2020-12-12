---
description: 'Дополнительные сведения о: is_trivially_copyable классе'
title: Класс is_trivially_copyable
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_trivially_copyable
helpviewer_keywords:
- is_trivially_copyable
ms.assetid: 89a53bf8-036c-4108-91e1-fe34adbde8b3
ms.openlocfilehash: 0c3590f1549f064492b361ae2ddeff665e9365ae
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97118476"
---
# <a name="is_trivially_copyable-class"></a>Класс is_trivially_copyable

Проверяет, является ли тип тривиально копируемым.

## <a name="syntax"></a>Синтаксис

```cpp
template <class T>
struct is_trivially_copyable;
```

### <a name="parameters"></a>Параметры

*T*\
Запрашиваемый тип.

## <a name="remarks"></a>Комментарии

Экземпляр предиката типа содержит значение true, если тип *T* является тривиальным копированием, в противном случае — значение false. Тривиально копируемые типы не имеют нетривиальных операций копирования, операций перемещения и деструкторов. Как правило, операция копирования считается тривиальной, если она может быть реализована как побитовое копирование. Встроенные типы и массивы тривиально копируемых типов являются тривиально копируемыми.

## <a name="requirements"></a>Требования

**Заголовок:**\<type_traits>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[<type_traits>](../standard-library/type-traits.md)
