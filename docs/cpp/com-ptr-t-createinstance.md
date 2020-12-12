---
description: 'Дополнительные сведения: _com_ptr_t:: CreateInstance'
title: _com_ptr_t::CreateInstance
ms.date: 11/04/2016
f1_keywords:
- _com_ptr_t::CreateInstance
helpviewer_keywords:
- CreateInstance method [C++]
ms.assetid: ab89b0e1-9da3-4784-a079-58b17340f111
ms.openlocfilehash: dd7ef236f25c22b25c9c083aea8439f5f5175d5b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97295527"
---
# <a name="_com_ptr_tcreateinstance"></a>_com_ptr_t::CreateInstance

**Блок, относящийся только к системам Microsoft**

Создает новый экземпляр объекта с заданным `CLSID` или `ProgID` .

## <a name="syntax"></a>Синтаксис

```
HRESULT CreateInstance(
   const CLSID& rclsid,
   IUnknown* pOuter=NULL,
   DWORD dwClsContext = CLSCTX_ALL
) throw( );
HRESULT CreateInstance(
   LPCWSTR clsidString,
   IUnknown* pOuter=NULL,
   DWORD dwClsContext = CLSCTX_ALL
) throw( );
HRESULT CreateInstance(
   LPCSTR clsidStringA,
   IUnknown* pOuter=NULL,
   DWORD dwClsContext = CLSCTX_ALL
) throw( );
```

#### <a name="parameters"></a>Параметры

*рклсид*<br/>
`CLSID`Объект объекта.

*клсидстринг*<br/>
Строка в Юникоде, которая содержит значение `CLSID` (начиная с "**{**") или `ProgID` .

*клсидстринга*<br/>
Многобайтовая строка, использующая кодовую страницу ANSI, которая содержит значение `CLSID` (начиная с "**{**") или `ProgID` .

*двклсконтекст*<br/>
Контекст для выполняющегося исполняемого кода.

*паутер*<br/>
Внешняя неизвестная для [агрегирования](../atl/aggregation.md).

## <a name="remarks"></a>Комментарии

Эти функции-члены вызывают `CoCreateInstance` для создания нового COM-объект, а затем запрашивают тип интерфейса данного интеллектуального указателя. Результирующий указатель затем инкапсулируется в этот объект `_com_ptr_t`. `Release` метод вызывается для уменьшения числа ссылок для ранее инкапсулированного указателя. Эта подпрограммы возвращает значение HRESULT для обозначения успеха или неудачи.

- **CreateInstance (**  *рклсид* **,**  *двклсконтекст*  **)** Создает новый выполняющийся экземпляр объекта, используя объект `CLSID` .

- **CreateInstance (**  *клсидстринг* **,**  *двклсконтекст*  **)** Создает новый запущенный экземпляр объекта с заданной строкой Юникода, содержащей значение `CLSID` (начиная с "**{**") или `ProgID` .

- **CreateInstance (**  *клсидстринга* **,**  *двклсконтекст*  **)** Создает новый запущенный экземпляр объекта с заданной строкой многобайтовых символов, содержащей либо `CLSID` (начиная с "**{**"), либо `ProgID` . Вызывает [MultiByteToWideChar](/windows/win32/api/stringapiset/nf-stringapiset-multibytetowidechar), который предполагает, что строка находится в кодовой странице ANSI, а не на кодовой странице OEM.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Класс _com_ptr_t](../cpp/com-ptr-t-class.md)
