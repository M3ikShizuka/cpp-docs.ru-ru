---
description: 'Дополнительные сведения о: структура Verifyinterfacehelper-'
title: VerifyInterfaceHelper - структура
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::VerifyInterfaceHelper
- implements/Microsoft::WRL::Details::VerifyInterfaceHelper::Verify
helpviewer_keywords:
- Microsoft::WRL::Details::VerifyInterfaceHelper structure
- Microsoft::WRL::Details::VerifyInterfaceHelper::Verify method
ms.assetid: ea95b641-199a-4fdf-964b-186b40cb3ba7
ms.openlocfilehash: a9b51eac55666d15b8362fc070d0feb731e9674d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97135035"
---
# <a name="verifyinterfacehelper-structure"></a>VerifyInterfaceHelper - структура

Поддерживает среда выполнения Windows инфраструктуру библиотеки шаблонов C++ и не предназначена для непосредственного использования в коде.

## <a name="syntax"></a>Синтаксис

```cpp
template <bool isWinRTInterface, typename I>
struct VerifyInterfaceHelper;

template <typename I>
struct VerifyInterfaceHelper<false, I>;
```

### <a name="parameters"></a>Параметры

*I*<br/>
Интерфейс для проверки.

*исвинртинтерфаце*

## <a name="remarks"></a>Комментарии

Проверяет, соответствует ли интерфейс, указанный параметром шаблона, определенным требованиям.

## <a name="members"></a>Элементы

### <a name="public-methods"></a>Открытые методы

name                                            | Описание
----------------------------------------------- | ---------------------------------------------------------------------------------------------------
[Метод VerifyInterfaceHelper::Verify](#verify) | Проверяет, отвечает ли определенным требованиям интерфейс, заданный текущим параметром шаблона.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`VerifyInterfaceHelper`

## <a name="requirements"></a>Требования

**Заголовок:** Implements. h

**Пространство имен:** Microsoft:: WRL::D состояния

## <a name="verifyinterfacehelperverify"></a><a name="verify"></a> Verifyinterfacehelper-:: Verify

Поддерживает инфраструктуру WRL и не предназначен для непосредственного использования в коде.

```cpp
static void Verify();
```

### <a name="remarks"></a>Комментарии

Проверяет, отвечает ли определенным требованиям интерфейс, заданный текущим параметром шаблона.
