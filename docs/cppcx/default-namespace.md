---
description: 'Дополнительные сведения: пространство имен по умолчанию'
title: Пространство имен default
ms.date: 12/30/2016
ms.assetid: 4712e9dc-57ba-43cc-811e-022e1dae4de8
ms.openlocfilehash: 46fa1e6162d0d9ffe25a47bfec88d8461f366828
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97273323"
---
# <a name="default-namespace"></a>Пространство имен default

`default`Пространство имен — это встроенные типы, поддерживаемые C++/CX.

## <a name="syntax"></a>Синтаксис

```
namespace default;
```

### <a name="members"></a>Члены

Все встроенные типы наследуют следующие члены.

| Имя | Описание |
|--|--|
| [default::(имя_типа)::Equals](../cppcx/default-type-name-equals-method.md) | Определяет, равен ли указанный объект текущему объекту. |
| [default::(имя_типа)::GetHashCode](../cppcx/default-type-name-gethashcode-method.md) | Возвращает хэш-код данного экземпляра. |
| [default::(имя_типа)::GetType](../cppcx/default-type-name-gettype-method.md) | Возвращает строку, которая представляет текущий тип. |
| [default::(имя_типа)::ToString](../cppcx/default-type-name-tostring-method.md) | Возвращает строку, которая представляет текущий тип. |

### <a name="built-in-types"></a>Встроенные типы

|Имя|Описание|
|----------|-----------------|
|`char16`|16-битовое нечисловое значение, представляющее кодовую точку Юникода (UTF-16).|
|`float32`|32-битовое число с плавающей запятой стандарта IEEE 754.|
|`float64`|64-битовое число с плавающей запятой стандарта IEEE 754.|
|`int16`|16-разрядное знаковое целое число.|
|`int32`|32-разрядное знаковое целое число.|
|`int64`|64-разрядное целое число со знаком.|
|`int8`|8-разрядное числовое значение со знаком.|
|`uint16`|16-разрядное целое число без знака.|
|`uint32`|32-разрядное целое число без знака.|
|`uint64`|64-разрядное целое число без знака.|
|`uint8`|8-разрядное числовое значение без знака.|

### <a name="requirements"></a>Требования

**Заголовок:** vccorlib.h

## <a name="see-also"></a>См. также раздел

[Справочник по языку C++/CX](../cppcx/visual-c-language-reference-c-cx.md)
