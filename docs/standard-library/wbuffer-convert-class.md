---
description: 'Дополнительные сведения о: wbuffer_convert классе'
title: Класс wbuffer_convert
ms.date: 11/04/2016
f1_keywords:
- xlocmon/stdext::cvt::wbuffer_convert
helpviewer_keywords:
- wbuffer_convert class
ms.assetid: 4a56f9bf-4138-4612-b516-525fea401358
ms.openlocfilehash: 1aa7258c3cc0a4f78a749f655e9cfb7cd4957378
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97187849"
---
# <a name="wbuffer_convert-class"></a>Класс wbuffer_convert

Описывает буфер потока, который управляет передачей элементов в буфер потока байтов и из него.

## <a name="syntax"></a>Синтаксис

```cpp
template <class Codecvt, class Elem = wchar_t, class Traits = std::char_traits<Elem>>
class wbuffer_convert
    : public std::basic_streambuf<Elem, Traits>
```

### <a name="parameters"></a>Параметры

*Codecvt*\
Аспект [языкового стандарта](../standard-library/locale-class.md), представляющий объект преобразования.

*Elem*\
Тип двухбайтового элемента.

*Признаки*\
Признаки, связанные с *Elem*.

## <a name="remarks"></a>Комментарии

Этот шаблон класса описывает буфер потока, который управляет передачей элементов типа `_Elem` , признаки символов которых описываются классом `Traits` , в буфер потока байтов типа и обратно `std::streambuf` .

Преобразование между последовательностями значений `Elem` и многобайтовыми последовательностями выполняется объектом класса `Codecvt<Elem, char, std::mbstate_t>`, который соответствует требованиям аспекта стандартного преобразования кода `std::codecvt<Elem, char, std::mbstate_t>`.

Объект этого шаблона класса хранит:

- указатель на базовый буфер потока байтов;

- Указатель на выделенный объект преобразования (освобождается при уничтожении объекта [wbuffer_convert](../standard-library/wbuffer-convert-class.md))
