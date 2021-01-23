---
description: Дополнительные сведения об pragma директиве const_seg в Microsoft C/C++
title: const_seg pragma
ms.date: 01/22/2021
f1_keywords:
- vc-pragma.const_seg
- const_seg_CPP
helpviewer_keywords:
- pragma, const_seg
- const_seg pragma
no-loc:
- pragma
ms.openlocfilehash: 602ef749c966f9b28d7d6fa42a2bded1148bbe0d
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98712925"
---
# <a name="const_seg-no-locpragma"></a>`const_seg` pragma

Указывает раздел (сегмент), в котором переменные [const](../cpp/const-cpp.md) хранятся в файле объекта (obj).

## <a name="syntax"></a>Синтаксис

> **`#pragma const_seg(`** ["*имя раздела*" [ **`,`** "*раздел-класс*"]] **`)`**\
> **`#pragma const_seg(`**{ **`push`**  |  **`pop`** } [ **`,`** *идентификатор* ] [ **`,`** "*раздел-имя*" [ **`,`** "*раздел-класс*"]]**`)`**

### <a name="parameters"></a>Параметры

**`push`**\
Используемых Помещает запись во внутренний стек компилятора. **`push`** Может иметь *идентификатор* и *имя раздела*.

**`pop`**\
Используемых Удаляет запись из верхнего внутреннего стека компилятора. **`pop`** Может иметь *идентификатор* и *имя раздела*. С помощью идентификатора можно открыть несколько записей, используя только одну **`pop`** команду . Имя *раздела* преобразуется в имя активного раздела const после точки подключения.

*identifier*\
Используемых При использовании с параметр **`push`** назначает имя записи во внутреннем стеке компилятора. При использовании с **`pop`** директива выводит записи из внутреннего стека до тех пор, пока *идентификатор* не будет удален. Если *идентификатор* не найден во внутреннем стеке, ничего не извлекается.

"*раздел-имя*" \
Используемых Имя раздела. При использовании с параметр **`pop`** Stack извлекается, а *имя раздела* становится активным именем раздела const.

"*класс-раздел*" \
Используемых Игнорируется, но входит в совместимость с версиями Microsoft C++, предшествующими версии 2,0.

## <a name="remarks"></a>Примечания

*Раздел* в объектном файле — это именованный блок данных, который загружается в память как единое целое. *Раздел const* — это раздел, содержащий постоянные данные. В этой статье термины *сегмент* и *раздел* имеют одинаковое значение.

**`const_seg`** pragma Директива указывает компилятору разместить все элементы постоянных данных из блока преобразования в раздел const с именем *section-name*. По умолчанию в объектном файле для **`const`** переменных используется раздел `.rdata` . Некоторые **`const`** переменные, такие как скалярные, автоматически встроены в поток кода. Встроенный код не отображается в `.rdata` . **`const_seg`** pragma Директива без параметра *name раздела* сбрасывает имя раздела для последующих **`const`** элементов данных до `.rdata` .

При определении объекта, для которого требуется динамическая инициализация `const_seg` , результат является неопределенным поведением.

Список имен, которые не следует использовать для создания раздела, см. в разделе [`/SECTION`](../build/reference/section-specify-section-attributes.md) .

Можно также указать разделы для инициализированных данных ( [`data_seg`](../preprocessor/data-seg.md) ), неинициализированных данных ( [`bss_seg`](../preprocessor/bss-seg.md) ) и функций ( [`code_seg`](../preprocessor/code-seg.md) ).

Для просмотра объектных файлов можно использовать приложение [DUMPBIN.EXE](../build/reference/dumpbin-command-line.md) . Версии DUMPBIN для каждой поддерживаемой целевой архитектуры входят в состав Visual Studio.

## <a name="example"></a>Пример

```cpp
// pragma_directive_const_seg.cpp
// compile with: /EHsc
#include <iostream>

const int i = 7;               // inlined, not stored in .rdata
const char sz1[]= "test1";     // stored in .rdata

#pragma const_seg(".my_data1")
const char sz2[]= "test2";     // stored in .my_data1

#pragma const_seg(push, stack1, ".my_data2")
const char sz3[]= "test3";     // stored in .my_data2

#pragma const_seg(pop, stack1) // pop stack1 from stack
const char sz4[]= "test4";     // stored in .my_data1

int main() {
    using namespace std;
   // const data must be referenced to be put in .obj
   cout << sz1 << endl;
   cout << sz2 << endl;
   cout << sz3 << endl;
   cout << sz4 << endl;
}
```

```Output
test1
test2
test3
test4
```

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
