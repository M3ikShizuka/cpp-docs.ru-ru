---
description: 'Дополнительные сведения о: _com_ptr_t:: Release'
title: _com_ptr_t::Release
ms.date: 11/04/2016
f1_keywords:
- _com_ptr_t.Release
- _com_ptr_t::Release
helpviewer_keywords:
- Release method [C++]
ms.assetid: db448b34-0efa-4f02-b701-ad1ca3ae6ca5
ms.openlocfilehash: a1b81295ab249b1826ea6d373f782d91765df3b7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97344722"
---
# <a name="_com_ptr_trelease"></a>_com_ptr_t::Release

**Блок, относящийся только к системам Microsoft**

Вызывает функцию члена **выпуска** `IUnknown` в указателе инкапсулированного интерфейса.

## <a name="syntax"></a>Синтаксис

```cpp
void Release( );
```

## <a name="remarks"></a>Remarks

Вызывает `IUnknown::Release` указатель на инкапсулированный интерфейс, вызывая `E_POINTER` ошибку, если этот указатель интерфейса имеет значение null.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _com_ptr_t](../cpp/com-ptr-t-class.md)
