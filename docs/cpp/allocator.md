---
description: 'Дополнительные сведения: `allocator`'
title: allocator
ms.date: 03/21/2019
f1_keywords:
- allocator_cpp
helpviewer_keywords:
- __declspec keyword [C++], allocator
- allocator __declspec keyword
ms.openlocfilehash: 20ca879259c49f01f5283a867b4e562cfddcc058
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97288273"
---
# `allocator`

**Блок, относящийся только к системам Microsoft**

**`allocator`** Спецификатор объявления можно применить к пользовательским функциям выделения памяти, чтобы сделать выделение видимым с помощью трассировки событий для Windows (ETW).

## <a name="syntax"></a>Синтаксис

> **`__declspec(allocator)`**

## <a name="remarks"></a>Remarks

Собственный профилировщик памяти в Visual Studio работает путем сбора данных событий ETW распределения, созданных во время выполнения. Распределители в CRT и пакете Windows SDK аннотированы на уровне исходного кода, что позволяет регистрировать их данные выделения. Если вы создаете собственные распределительы, то любые функции, возвращающие указатель на только что выделенную память кучи, могут быть дополнены с помощью `__declspec(allocator)` , как показано в следующем примере для myMalloc:

```cpp
__declspec(allocator) void* myMalloc(size_t size)
```

Дополнительные сведения см. [в разделе измерение использования памяти в Visual Studio](/visualstudio/profiling/memory-usage) и [пользовательские события кучи ETW для машинного кода](/visualstudio/profiling/custom-native-etw-heap-events).

**Завершение блока, относящегося только к системам Майкрософт**
