---
description: 'Дополнительные сведения о: time_put_byname классе'
title: Класс time_put_byname
ms.date: 11/04/2016
f1_keywords:
- xloctime/std::time_put_byname
helpviewer_keywords:
- time_put_byname class
ms.assetid: e08c2348-64d2-4ace-98b1-1496e14c7b1a
ms.openlocfilehash: b519b28b7af8f5b54f9150d1d84f68cd6695bc49
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97167257"
---
# <a name="time_put_byname-class"></a>Класс time_put_byname

Шаблон производного класса описывает объект, который может выступать в качестве аспекта языкового стандарта типа `time_put` \< CharType, OutputIterator > .

## <a name="syntax"></a>Синтаксис

```cpp
template <class CharType, class OutIt = ostreambuf_iterator<CharType, char_traits<CharType>>>
class time_put_byname : public time_put<CharType, OutputIterator>
{
public:
    explicit time_put_byname(
    const char* _Locname,
    size_t _Refs = 0);

    explicit time_put_byname(
    const string& _Locname,
    size_t _Refs = 0);

protected:
    virtual ~time_put_byname();

};
```

### <a name="parameters"></a>Параметры

*_Locname*\
Имя языкового стандарта.

*_Refs*\
Начальное значение счетчика ссылок.

## <a name="remarks"></a>Комментарии

Его поведение определяется с помощью [именованного](../standard-library/locale-class.md#name) языкового стандарта *_Locname*. Каждый конструктор инициализирует свой базовый объект с помощью [time_put](../standard-library/time-put-class.md#time_put) \<CharType, OutputIterator> ( `_Refs` ).

## <a name="requirements"></a>Требования

**Заголовок:**\<locale>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
