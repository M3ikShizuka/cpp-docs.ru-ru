---
description: 'Дополнительные сведения о: _U_RECT классе'
title: Класс _U_RECT
ms.date: 11/04/2016
f1_keywords:
- ATL::_U_RECT
- _U_RECT
- ATL._U_RECT
helpviewer_keywords:
- U_RECT class
- _U_RECT class
ms.assetid: 5f880a2d-09cf-4327-bf32-a3519c4dcd63
ms.openlocfilehash: b3720107d1b64f930b4c64dff269de041d9b928c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97157611"
---
# <a name="_u_rect-class"></a>Класс _U_RECT

Этот класс адаптера Argument позволяет `RECT` передавать указатели или ссылки в функцию, которая реализуется в терминах указателей.

> [!IMPORTANT]
> Этот класс и его члены не могут использоваться в приложениях, выполняемых в среда выполнения Windows.

## <a name="syntax"></a>Синтаксис

```
class _U_RECT
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[_U_RECT:: _U_RECT](#_u_rect___u_rect)|Конструктор.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[_U_RECT:: m_lpRect](#_u_rect__m_lprect)|Указатель на `RECT` .|

## <a name="remarks"></a>Комментарии

Класс определяет две перегрузки конструктора: один принимает аргумент **RECT&** , а другой принимает `LPRECT` аргумент. Первый конструктор сохраняет адрес ссылочного аргумента в одном элементе данных класса, [m_lpRect](#_u_rect__m_lprect). Аргумент для конструктора указателя сохраняется непосредственно без преобразования.

## <a name="requirements"></a>Требования

**Заголовок:** atlwin. h

## <a name="_u_rectm_lprect"></a><a name="_u_rect__m_lprect"></a> _U_RECT:: m_lpRect

Класс содержит значение, передаваемое в любой из его конструкторов как открытый `LPRECT` элемент данных.

```
LPRECT m_lpRect;
```

## <a name="_u_rect_u_rect"></a><a name="_u_rect___u_rect"></a> _U_RECT:: _U_RECT

Адрес ссылочного аргумента хранится в одном элементе данных класса, [m_lpRect](#_u_rect__m_lprect).

```
_U_RECT(RECT& rc);
_U_RECT(LPRECT lpRect);
```

### <a name="parameters"></a>Параметры

*RC*<br/>
Ссылка `RECT`.

*лпрект*<br/>
`RECT`Указатель.

### <a name="remarks"></a>Комментарии

Аргумент для конструктора указателя сохраняется непосредственно без преобразования.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../atl/atl-class-overview.md)
