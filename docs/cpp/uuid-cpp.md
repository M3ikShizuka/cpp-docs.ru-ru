---
description: 'Дополнительные сведения: UUID (C++)'
title: uuid (C++)
ms.date: 11/04/2016
f1_keywords:
- uuid_cpp
helpviewer_keywords:
- __declspec keyword [C++], uuid
- uuid __declspec keyword
ms.assetid: 9d004621-09bc-4a8d-871b-648f5d5102d7
ms.openlocfilehash: c841bb1813769ab70e756fe4edb7fd351c1dbc49
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97116734"
---
# <a name="uuid-c"></a>uuid (C++)

**Блок, относящийся только к системам Microsoft**

Компилятор присоединяет идентификатор GUID к классу или структуре, объявленным или определенным (только для определений полных объектов COM) с **`uuid`** атрибутом.

## <a name="syntax"></a>Синтаксис

```
__declspec( uuid("ComObjectGUID") ) declarator
```

## <a name="remarks"></a>Remarks

**`uuid`** Атрибут принимает в качестве аргумента строку. Эта строка присваивает идентификатор GUID в стандартном формате реестра с разделителями **{}** или без них. Пример:

```cpp
struct __declspec(uuid("00000000-0000-0000-c000-000000000046")) IUnknown;
struct __declspec(uuid("{00020400-0000-0000-c000-000000000046}")) IDispatch;
```

Этот атрибут можно применить при повторном объявлении. Это позволяет заголовкам систем предоставлять определения интерфейсов `IUnknown` , например, и повторное объявление в каком-либо другом заголовке (например, \<comdef.h> ) для предоставления идентификатора GUID.

Ключевое слово [__uuidof](../cpp/uuidof-operator.md) можно применить для получения постоянного GUID, присоединенного к определяемому пользователем типу.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[__declspec](../cpp/declspec.md)<br/>
[Ключевые слова](../cpp/keywords-cpp.md)
