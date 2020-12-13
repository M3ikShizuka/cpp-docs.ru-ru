---
description: 'Дополнительные сведения о: структура метод verifyinheritancehelper'
title: VerifyInheritanceHelper - структура
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::VerifyInheritanceHelper
- implements/Microsoft::WRL::Details::VerifyInheritanceHelper::Verify
helpviewer_keywords:
- Microsoft::WRL::Details::VerifyInheritanceHelper structure
- Microsoft::WRL::Details::VerifyInheritanceHelper::Verify method
ms.assetid: 8a48a702-0f71-4807-935b-8311f0a7a8b6
ms.openlocfilehash: 672455482a2d21cb695124cad31740b6325c377d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97135048"
---
# <a name="verifyinheritancehelper-structure"></a>VerifyInheritanceHelper - структура

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
template <typename I, typename Base>
struct VerifyInheritanceHelper;

template <typename I>
struct VerifyInheritanceHelper<I, Nil>;
```

### <a name="parameters"></a>Параметры

*I*<br/>
Тип.

*Из*<br/>
Другой тип.

## <a name="remarks"></a>Комментарии

Проверяет, является ли один интерфейс производным от другого интерфейса.

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

name                                       | Описание
------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------
[Метод verifyinheritancehelper:: Verify](#verify) | Проверяет два интерфейса, указанные текущими параметрами шаблона, и определяет, является ли один интерфейс производным от другого.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`VerifyInheritanceHelper`

## <a name="requirements"></a>Требования

**Заголовок:** Implements. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="verifyinheritancehelperverify"></a><a name="verify"></a> Метод verifyinheritancehelper:: Verify

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
static void Verify();
```

### <a name="remarks"></a>Комментарии

Проверяет два интерфейса, указанные текущими параметрами шаблона, и определяет, является ли один интерфейс производным от другого.

Если это условие не выполняется, выдается ошибка.
