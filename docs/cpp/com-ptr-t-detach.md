---
description: 'Дополнительные сведения: _com_ptr_t::D етач'
title: _com_ptr_t::Detach
ms.date: 11/04/2016
f1_keywords:
- _com_ptr_t::Detach
helpviewer_keywords:
- Detach method [C++]
ms.assetid: 0652053e-af37-44e9-a278-2522212ebfed
ms.openlocfilehash: ec2a18a04b8c32e373225235fd0d6f520e768af0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97295514"
---
# <a name="_com_ptr_tdetach"></a>_com_ptr_t::Detach

**Блок, относящийся только к системам Microsoft**

Извлекает и возвращает инкапсулированный указатель на интерфейс.

## <a name="syntax"></a>Синтаксис

```
Interface* Detach( ) throw( );
```

## <a name="remarks"></a>Remarks

Извлекает и возвращает инкапсулированный указатель на интерфейс, а затем очищает область хранения инкапсулированного указателя, присваивая ему значение NULL. Поэтому указатель на интерфейс удаляется из инкапсуляции. Вы должны вызвать метод `Release` в возвращенном указателе интерфейса.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _com_ptr_t](../cpp/com-ptr-t-class.md)
