---
description: 'Дополнительные сведения: Синхронизация'
title: Synchronize (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.synchronize
helpviewer_keywords:
- synchronize attribute
ms.assetid: 15fc8544-955d-4765-b3d5-0f619c8b3f40
ms.openlocfilehash: bbee19406396e4041b4d7ca1e2acf2b8d7193494
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97329558"
---
# <a name="synchronize"></a>synchronize

Синхронизирует доступ к целевому методу.

## <a name="syntax"></a>Синтаксис

```cpp
[synchronize]
```

## <a name="remarks"></a>Remarks

Атрибут **Synchronize** C++ реализует поддержку синхронизации целевого метода объекта. Синхронизация позволяет нескольким объектам использовать общий ресурс (например, метод класса), управляя доступом к целевому методу.

Код, вставленный этим атрибутом, вызывает правильный `Lock` метод (определяется потоковой моделью) в начале целевого метода. При завершении работы метода `Unlock` вызывается автоматически. Дополнительные сведения об этих функциях см. в разделе [ккомаутосреадмодуле:: Lock.](../../atl/reference/ccomautothreadmodule-class.md#lock)

Этот атрибут требует, чтобы атрибут [coclass](coclass.md), [progid](progid.md)или [vi_progid](vi-progid.md) (или другой атрибут, который подразумевает один из них) также применялся к этому элементу. Если используется любой отдельный атрибут, два других применяются автоматически. Например, если `progid` применяется, то применяются `vi_progid` `coclass` также и.

## <a name="example"></a>Пример

Следующий код обеспечивает синхронизацию для `UpdateBalance` метода `CMyClass` объекта.

```cpp
// cpp_attr_ref_synchronize.cpp
// compile with: /LD
#define _ATL_ATTRIBUTES
#include "atlbase.h"
#include "atlcom.h"

[module(name="SYNC")];

[coclass,
threading(both),
vi_progid("MyProject.MyClass"),
progid("MyProject.MyClass.1"),
uuid("7a7baa0d-59b8-4576-b754-79d07e1d1cc3")
]
class CMyClass {
   float m_nBalance;

   [synchronize]
   void UpdateBalance(float nAdjust) {
      m_nBalance += nAdjust;
   }
};
```

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|Метод класса, метод|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Один или несколько из следующих элементов: `coclass` , `progid` или `vi_progid` .|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты COM](com-attributes.md)
