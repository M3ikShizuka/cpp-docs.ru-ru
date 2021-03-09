---
description: 'Дополнительные сведения: no_sanitize_address'
title: no_sanitize_address
ms.date: 11/04/2016
f1_keywords:
- no_sanitize_address__cpp
helpviewer_keywords:
- __declspec keyword [C++], no_sanitize_address
- no_sanitize_address __declspec keyword
ms.openlocfilehash: a18b60f666bc53ef72db3a6d230dc7531cc6bc1f
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471198"
---
# `no_sanitize_address`

**Блок, относящийся только к системам Microsoft**

**`__declspec(no_sanitize_address)`** Описатель сообщает компилятору, что следует отключить очистку адреса для функций, локальных переменных или глобальных переменных. Этот описатель используется в сочетании с [аддресссанитизер](../sanitizers/asan.md).

> [!NOTE]
> **`__declspec(no_sanitize_address)`** отключает поведение _компилятора_ , а не поведения *среды выполнения* .

## <a name="example"></a>Пример

Примеры см. в [справочнике по сборке аддресссанитизер](../sanitizers/asan-building.md#__declspecno_sanitize_address) .

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[`__declspec`](../cpp/declspec.md)\
[Словами](../cpp/keywords-cpp.md)\
[аддресссанитизер](../sanitizers/asan.md)
