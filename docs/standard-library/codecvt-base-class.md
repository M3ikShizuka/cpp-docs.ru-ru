---
description: 'Дополнительные сведения о: codecvt_base классе'
title: Класс codecvt_base
ms.date: 11/04/2016
f1_keywords:
- xlocale/std::codecvt_base
helpviewer_keywords:
- codecvt_base class
ms.assetid: 7e95c083-91b4-4b3f-8918-0d4ea244a040
ms.openlocfilehash: d0fb5a56a163ba80cee89eb6f37200243e6c08e5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97325105"
---
# <a name="codecvt_base-class"></a>Класс codecvt_base

Базовый класс для класса codecvt, который используется для определения типа перечисления, который называется `result` , используется в качестве возвращаемого типа для функций-членов аспекта для указания результата преобразования.

## <a name="syntax"></a>Синтаксис

```cpp
class codecvt_base : public locale::facet {
public:
    enum result {ok, partial, error, noconv};
    codecvt_base( size_t _Refs = 0);
    bool always_noconv() const;
    int max_length() const;
    int encoding() const;
    ~codecvt_base()

protected:
    virtual bool do_always_noconv() const;
    virtual int do_max_length() const;
    virtual int do_encoding() const;
};
```

## <a name="remarks"></a>Remarks

Класс описывает перечисление, общее для всех специализаций шаблона класса [codecvt](../standard-library/codecvt-class.md). Результат перечисления описывает возможные возвращаемые значения из [do_in](../standard-library/codecvt-class.md#do_in) или [do_out](../standard-library/codecvt-class.md#do_out):

- `ok` Если преобразование между внутренними и внешними кодировками символов выполнено.

- `partial` значение, если назначение недостаточно велико для успешности преобразования.

- `error` значение, если исходная последовательность сформирована неправильно.

- `noconv`, если функция не выполняет преобразование;

## <a name="requirements"></a>Требования

**Заголовок:**\<locale>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Безопасность потоков в стандартной библиотеке C++](../standard-library/thread-safety-in-the-cpp-standard-library.md)
