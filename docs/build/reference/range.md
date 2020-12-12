---
description: Дополнительные сведения о:/РАНЖЕ
title: Параметр /RANGE
ms.date: 11/04/2016
f1_keywords:
- /RANGE
helpviewer_keywords:
- /RANGE dumpbin option
- -RANGE dumpbin option
ms.assetid: 7eeba266-32be-49cc-a350-96bdf541f98a
ms.openlocfilehash: 9af54bddde977e92b5256f0835c31afbff1405d4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97225405"
---
# <a name="range"></a>Параметр /RANGE

Изменяет выходные данные DUMPBIN при использовании с другими параметрами DUMPBIN, например/РАВДАТА или/ДИСАСМ.

## <a name="syntax"></a>Синтаксис

```
/RANGE:vaMin[,vaMax]
```

## <a name="parameters"></a>Параметры

*вамин*<br/>
Виртуальный адрес, с которого начинается операция dumpbin.

*вамакс*<br/>
Используемых Виртуальный адрес, по которому должна завершиться операция dumpbin. Если не указано, программа DUMPBIN перейдет в конец файла.

## <a name="remarks"></a>Комментарии

Чтобы просмотреть виртуальные адреса образа, используйте файл отображения для образа (RVA + Base), параметр **/DISASM** или **/headers** программы DUMPBIN или окно дизассемблирования в отладчике Visual Studio.

## <a name="example"></a>Пример

В этом примере **/ранже** используется для изменения режима вывода параметра **/DISASM** . В этом примере начальное значение выражается десятичным числом, а конечное значение указывается в виде шестнадцатеричного числа.

```
dumpbin /disasm /range:4219334,0x004061CD t.exe
```

## <a name="see-also"></a>См. также раздел

[Параметры DUMPBIN](dumpbin-options.md)
