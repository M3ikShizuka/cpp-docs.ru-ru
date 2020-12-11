---
description: Дополнительные сведения о &lt; &gt; функциях IStream.
title: Функции &lt;istream&gt;
ms.date: 11/04/2016
f1_keywords:
- istream/std::swap
- istream/std::ws
ms.assetid: 0301ea0d-4ded-4841-83dd-4253b55b3188
ms.openlocfilehash: c71770d8c6e86829eb4e0153abc924d612d3eff6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97154179"
---
# <a name="ltistreamgt-functions"></a>Функции &lt;istream&gt;

[позиции](#istream_swap)\
[ws](#ws)

## <a name="swap"></a><a name="istream_swap"></a> позиции

Меняет местами элементы двух объектов-потоков.

```cpp
template <class Elem, class Tr>
void swap(
    basic_istream<Elem, Tr>& left,
    basic_istream<Elem, Tr>& right);

template <class Elem, class Tr>
void swap(
    basic_iostream<Elem, Tr>& left,
    basic_iostream<Elem, Tr>& right);
```

### <a name="parameters"></a>Параметры

*слева*\
Поток.

*Правильно*\
Поток.

## <a name="ws"></a><a name="ws"></a> Протокол

Пропускает пробелы в потоке.

```cpp
template class<Elem, Tr> basic_istream<Elem, Tr>& ws(basic_istream<Elem, Tr>& _Istr);
```

### <a name="parameters"></a>Параметры

*_Istr*\
Поток.

### <a name="return-value"></a>Возвращаемое значение

Поток.

### <a name="remarks"></a>Комментарии

Манипулятор извлекает и удаляет все элементы `ch` , для которых [use_facet](../standard-library/basic-filebuf-class.md#open) <  **CType** \< **Elem**> > ( [getloc](../standard-library/ios-base-class.md#getloc)). **имеет** значение true ( **CType** \< **Elem**> :: **Space**, **CH**).

Функция вызывает [setstate](../standard-library/basic-ios-class.md#setstate)( **eofbit**) при обнаружении конца файла при извлечении элементов. Он возвращает *_Istr*.

### <a name="example"></a>Пример

См. раздел [оператор>>](../standard-library/istream-operators.md#op_gt_gt) с примером использования `ws`.

## <a name="see-also"></a>См. также раздел

[\<istream>](../standard-library/istream.md)
