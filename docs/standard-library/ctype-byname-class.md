---
description: 'Дополнительные сведения о: ctype_byname классе'
title: Класс ctype_byname
ms.date: 11/04/2016
f1_keywords:
- xlocale/std::ctype_byname
helpviewer_keywords:
- ctype_byname class
ms.assetid: a5cec021-a1f8-425f-8757-08e6f064b604
ms.openlocfilehash: cc5f44e1c544d2088030621b684c9e070175d695
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97233140"
---
# <a name="ctype_byname-class"></a>Класс ctype_byname

Шаблон производного класса описывает объект, который может служить в качестве аспекта ctype данного языкового стандарта, позволяя классифицировать символы и преобразование символов между вариантами Case и native и Locale, заданными наборами символов.

## <a name="syntax"></a>Синтаксис

```cpp
template <class _Elem>
class ctype_byname : public ctype<_Elem>
{
public:
    explicit ctype_byname(
    const char* _Locname,
    size_t _Refs = 0);

    explicit ctype_byname(
    const string& _Locname,
    size_t _Refs = 0);

protected:
    virtual __CLR_OR_THIS_CALL ~ctype_byname();

};
```

## <a name="remarks"></a>Remarks

Его поведение определяется именованным языковым стандартом `_Locname`. Каждый конструктор инициализирует свой базовый объект с помощью [CType](../standard-library/ctype-class.md) \<CharType> ( `_Refs` ) или эквивалента для базового класса `ctype<char>` .

## <a name="requirements"></a>Требования

**Заголовок:**\<locale>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
