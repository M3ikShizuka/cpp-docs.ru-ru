---
description: 'Дополнительные сведения: _com_ptr_t:: QueryInterface'
title: _com_ptr_t::QueryInterface
ms.date: 11/04/2016
f1_keywords:
- _com_ptr_t::QueryInterface
- _com_ptr_t.QueryInterface
helpviewer_keywords:
- QueryInterface method [C++]
ms.assetid: d03292f1-6b02-40db-9756-8b0837a97319
ms.openlocfilehash: 6c6ff19227c920aade762af295942d8058a17ad3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97295345"
---
# <a name="_com_ptr_tqueryinterface"></a>_com_ptr_t::QueryInterface

**Блок, относящийся только к системам Microsoft**

Вызывает функцию члена **QueryInterface** `IUnknown` в указателе инкапсулированного интерфейса.

## <a name="syntax"></a>Синтаксис

```
template<typename _InterfaceType> HRESULT QueryInterface (
   const IID& iid,
   _InterfaceType*& p
) throw ( );
template<typename _InterfaceType> HRESULT QueryInterface (
   const IID& iid,
   _InterfaceType** p
) throw( );
```

#### <a name="parameters"></a>Параметры

*IID*<br/>
`IID` указателя интерфейса.

*p*<br/>
Необработанный указатель на интерфейс.

## <a name="remarks"></a>Комментарии

Вызывает `IUnknown::QueryInterface` указатель инкапсулированного интерфейса с указанным `IID` и возвращает полученный указатель необработанного интерфейса в *p*. Эта подпрограммы возвращает значение HRESULT для обозначения успеха или неудачи.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _com_ptr_t](../cpp/com-ptr-t-class.md)
