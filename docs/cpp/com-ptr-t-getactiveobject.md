---
description: 'Дополнительные сведения: _com_ptr_t:: Жетактивеобжект'
title: _com_ptr_t::GetActiveObject
ms.date: 11/04/2016
f1_keywords:
- _com_ptr_t::GetActiveObject
helpviewer_keywords:
- GetActiveObject method [C++]
ms.assetid: 2fa94853-0410-4620-91f2-136dae923f9f
ms.openlocfilehash: 96784e73d91d7be4b0674e09278183fc62e60af2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97295475"
---
# <a name="_com_ptr_tgetactiveobject"></a>_com_ptr_t::GetActiveObject

**Блок, относящийся только к системам Microsoft**

Присоединяет к существующему экземпляру объекта, заданному `CLSID` или `ProgID` .

## <a name="syntax"></a>Синтаксис

```
HRESULT GetActiveObject(
   const CLSID& rclsid
) throw( );
HRESULT GetActiveObject(
   LPCWSTR clsidString
) throw( );
HRESULT GetActiveObject(
   LPCSTR clsidStringA
) throw( );
```

#### <a name="parameters"></a>Параметры

*рклсид*<br/>
`CLSID`Объект объекта.

*клсидстринг*<br/>
Строка в Юникоде, которая содержит значение `CLSID` (начиная с "**{**") или `ProgID` .

*клсидстринга*<br/>
Многобайтовая строка, использующая кодовую страницу ANSI, которая содержит значение `CLSID` (начиная с "**{**") или `ProgID` .

## <a name="remarks"></a>Комментарии

Эти функции-члены вызывают **жетактивеобжект** , чтобы получить указатель на запущенный объект, зарегистрированный в OLE, а затем запрашивает тип интерфейса этого интеллектуального указателя. Результирующий указатель затем инкапсулируется в этот объект `_com_ptr_t`. `Release` метод вызывается для уменьшения числа ссылок для ранее инкапсулированного указателя. Эта подпрограммы возвращает значение HRESULT для обозначения успеха или неудачи.

- **Жетактивеобжект (** `rclsid` **)** подключается к существующему экземпляру объекта, заданному `CLSID` .    

- **Жетактивеобжект (** `clsidString` **)** подключается к существующему экземпляру объекта при наличии строки в Юникоде, содержащей значение `CLSID` (начиная с "**{**") или `ProgID` .    

- **Жетактивеобжект (** `clsidStringA` **)** подключается к существующему экземпляру объекта при наличии строки многобайтовых символов, содержащей значение `CLSID` (начиная с "**{**") или `ProgID` .     Вызывает [MultiByteToWideChar](/windows/win32/api/stringapiset/nf-stringapiset-multibytetowidechar), который предполагает, что строка находится в кодовой странице ANSI, а не на кодовой странице OEM.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _com_ptr_t](../cpp/com-ptr-t-class.md)
