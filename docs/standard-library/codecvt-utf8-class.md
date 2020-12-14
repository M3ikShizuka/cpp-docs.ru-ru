---
description: 'Дополнительные сведения: codecvt_utf8'
title: codecvt_utf8
ms.date: 11/04/2016
f1_keywords:
- codecvt/std::codecvt_utf8
helpviewer_keywords:
- codecvt_utf8 class
ms.assetid: 2a87478f-e2d4-4b8d-ad9c-00add01d1bb0
ms.openlocfilehash: b0da37607d563786285564d17b2c8a49e9e064bf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97234037"
---
# <a name="codecvt_utf8"></a>codecvt_utf8

Представляет аспект [языкового стандарта](../standard-library/locale-class.md) , который выполняет преобразование между расширенными символами в кодировке UCS-2 или UCS-4 и потоком байтов в кодировке UTF-8.

```cpp
template<class Elem, unsigned long Maxcode = 0x10ffff, codecvt_mode Mode = (codecvt_mode)0>
class codecvt_utf8 : public std::codecvt<Elem, char, StateType>
```

## <a name="parameters"></a>Параметры

*Elem*\
Тип двухбайтового элемента.

*макскоде*\
Максимальное количество символов для аспекта языкового стандарта.

*Режима*\
Сведения о конфигурации для аспекта языкового стандарта.

## <a name="remarks"></a>Комментарии

Поток байтов может записываться в двоичный файл или текстовый файл.

## <a name="requirements"></a>Требования

Заголовок: \<codecvt>

Пространство имен: std
