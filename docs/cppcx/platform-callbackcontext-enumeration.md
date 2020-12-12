---
description: 'См. Дополнительные сведения о перечислении Platform:: CallbackContext'
title: Platform::CallbackContext - перечисление
ms.date: 12/30/2016
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::CallbackContext
helpviewer_keywords:
- Platform::CallbackContext Enumeration
ms.assetid: 60e0c7cb-5d8f-482a-bdca-ca9335ae4899
ms.openlocfilehash: 36c30b674065f42f7d50a403d1506344ffcfecac
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97170975"
---
# <a name="platformcallbackcontext-enumeration"></a>Platform::CallbackContext - перечисление

Указывает контекст потока, в котором выполняется функция обратного вызова (обработчик события).

## <a name="syntax"></a>Синтаксис

```cpp
enum class CallbackContext {};
```

### <a name="members"></a>Члены

|Код типа|Описание|
|---------------|-----------------|
|Любой|Функция обратного вызова может выполняться в любом контексте потока.|
|Аналогично|Функция обратного вызова может выполняться в контексте потока, запустившего асинхронную операцию.|

### <a name="requirements"></a>Требования

**Минимальный поддерживаемый клиент:** Windows 8

**Минимальный поддерживаемый сервер:** Windows Server 2012

**Пространство имен:** Platform

**Метаданные:** Platform. winmd
