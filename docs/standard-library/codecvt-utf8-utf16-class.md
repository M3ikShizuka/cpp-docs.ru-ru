---
description: 'Дополнительные сведения: codecvt_utf8_utf16'
title: codecvt_utf8_utf16
ms.date: 11/04/2016
f1_keywords:
- codecvt/std::cvt_utf8_utf16
helpviewer_keywords:
- codecvt_utf8_utf16 class
ms.assetid: 4c12c881-5dba-4e39-b338-0b9caff5af29
ms.openlocfilehash: e80cdaa01ef77b9ce28a773eb4e05056220718a7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97325079"
---
# <a name="codecvt_utf8_utf16"></a>codecvt_utf8_utf16

Представляет аспект [языкового стандарта](../standard-library/locale-class.md) , который выполняет преобразование между расширенными символами в кодировке UTF-16 и потоком байтов в кодировке UTF-8.

```cpp
template<class Elem, unsigned long Maxcode = 0x10ffff, codecvt_mode Mode = (codecvt_mode)0>
class codecvt_utf8_utf16 : public _STD codecvt<Elem, char, StateType>
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
