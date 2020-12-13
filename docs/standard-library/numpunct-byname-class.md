---
description: 'Дополнительные сведения о: numpunct_byname классе'
title: Класс numpunct_byname
ms.date: 11/04/2016
f1_keywords:
- xlocnum/std::numpunct_byname
helpviewer_keywords:
- numpunct_byname class
ms.assetid: 18412924-e085-4771-b5e9-7a200cbdd7c0
ms.openlocfilehash: e4e6352f9f65b2a726acf3f8f5f8ede9bffe54f9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338036"
---
# <a name="numpunct_byname-class"></a>Класс numpunct_byname

Шаблон производного класса описывает объект, который можно использовать в качестве `numpunct` аспекта заданного языкового стандарта, который включает форматирование и пунктуацию числовых и логических выражений.

## <a name="syntax"></a>Синтаксис

```cpp
template <class CharType>
class numpunct_byname : public numpunct<Elem> {
public:
    explicit numpunct_byname(
    const char* _Locname,
    size_t _Refs = 0);

    explicit numpunct_byname(
    const string& _Locname,
    size_t _Refs = 0);

protected:
    virtual ~numpunct_byname();

};
```

## <a name="remarks"></a>Remarks

Его поведение определяется [с помощью именованного](../standard-library/locale-class.md#name) языкового стандарта `_Locname` . Конструктор инициализирует свой базовый объект с помощью [numpunct](../standard-library/numpunct-class.md#numpunct) \<CharType> ( `_Refs` ).

## <a name="requirements"></a>Требования

**Заголовок:**\<locale>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
