---
description: 'Дополнительные сведения о: _com_ptr_t:: AddRef'
title: _com_ptr_t::AddRef
ms.date: 11/04/2016
f1_keywords:
- _com_ptr_t::AddRef
helpviewer_keywords:
- AddRef method [C++], interface pointers
ms.assetid: c104dac3-aad3-40bb-a298-75c6cd0e63a2
ms.openlocfilehash: 0979245662a94596307b1a63af918d0ce67c7b6f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97295696"
---
# <a name="_com_ptr_taddref"></a>_com_ptr_t::AddRef

**Блок, относящийся только к системам Microsoft**

Вызывает `AddRef` функцию члена `IUnknown` в инкапсулированном указателе интерфейса.

## <a name="syntax"></a>Синтаксис

```cpp
void AddRef( );
```

## <a name="remarks"></a>Remarks

Вызывает `IUnknown::AddRef` указатель на инкапсулированный интерфейс, вызывая `E_POINTER` ошибку, если указатель имеет значение null.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _com_ptr_t](../cpp/com-ptr-t-class.md)
