---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 4) C4435'
title: Предупреждение компилятора (уровень 4) C4435
ms.date: 11/04/2016
f1_keywords:
- C4435
helpviewer_keywords:
- C4435
ms.assetid: a04524af-2b71-4ff9-9729-d9d1d1904ed7
ms.openlocfilehash: ce5ee4e32f6efa1e7986d55fafa0ceec8b754351
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97203514"
---
# <a name="compiler-warning-level-4-c4435"></a>Предупреждение компилятора (уровень 4) C4435

"class1": структура объекта в /vd2 изменится из-за виртуального базового класса "class2"

Это предупреждение отключено по умолчанию. Подробнее: [Выключенные по умолчанию предупреждения компилятора](../../preprocessor/compiler-warnings-that-are-off-by-default.md) .

В параметре компиляции по умолчанию/vd1 производный класс не имеет `vtordisp` поля для указанного виртуального базового объекта.  Если/vd2 или `#pragma vtordisp(2)` действует, `vtordisp` появится поле, изменяющее макет объекта.  Это может привести к проблемам совместимости с двоичными данными, если взаимодействующие модули компилируются с разными `vtordisp` параметрами.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C4435.

```cpp
// C4435.cpp
// compile with: /c /W4
#pragma warning(default : 4435)
class A
{
public:
    virtual ~A() {}
};

class B : public virtual A  // C4435
{};
```

## <a name="see-also"></a>См. также раздел

[vtordisp](../../preprocessor/vtordisp.md)<br/>
[/ВД (отключение замещения конструкций)](../../build/reference/vd-disable-construction-displacements.md)
