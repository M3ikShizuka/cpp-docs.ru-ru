---
description: 'Дополнительные сведения о: bad_any_cast классе'
title: Класс bad_any_cast
ms.date: 04/04/2019
f1_keywords:
- any/std::bad_any_cast
- any/std::bad_any_cast::what
helpviewer_keywords:
- any/std::bad_any_cast
- any/std::bad_any_cast::what
ms.openlocfilehash: 5b38405bf1fc826592995df4037c5853e88ad9eb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321631"
---
# <a name="bad_any_cast-class"></a>Класс bad_any_cast

Объекты, созданные при сбое `any_cast` .

## <a name="syntax"></a>Синтаксис

```cpp
class bad_any_cast
```

### <a name="member-functions"></a>Функции элементов

|Имя|Описание|
|-|-|
|[What](#what)|Возвращает тип.|

## <a name="what"></a><a name="what"></a> What

Возвращает тип.

```cpp
const char* what() const noexcept override;
```
