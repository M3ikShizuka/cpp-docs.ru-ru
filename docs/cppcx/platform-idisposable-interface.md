---
description: 'Дополнительные сведения об интерфейсе Platform:: IDisposable'
title: Platform::IDisposable - интерфейс
ms.date: 02/03/2017
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::IDisposable
helpviewer_keywords:
- Platform::IDisposable Interface
ms.assetid: f4344056-7030-42ed-bc98-b140edffddcd
ms.openlocfilehash: 0a1e7b44861d48f496f21d634d4d28ff1c968bcf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97276781"
---
# <a name="platformidisposable-interface"></a>Platform::IDisposable - интерфейс

Используется для освобождения неуправляемых ресурсов.

## <a name="syntax"></a>Синтаксис

```cpp
public interface class IDisposable
```

## <a name="attributes"></a>Атрибуты

**GuidAttribute**("de0cbaea-8065-4a45-b196-c9d443f9bab3")

**Версионаттрибуте**(NTDDI_WIN8)

### <a name="members"></a>Элементы

Интерфейс IDisposable наследует от интерфейса IUnknown. Интерфейс IDisposable также имеет следующие типы членов.

**Методы**

Интерфейс IDisposable содержит следующие методы.

|Метод|Описание|
|------------|-----------------|
|Dispose|Используется для освобождения неуправляемых ресурсов.|

### <a name="requirements"></a>Требования

**Минимальный поддерживаемый клиент:** Windows 8

**Минимальный поддерживаемый сервер:** Windows Server 2012

**Пространство имен:** Platform
