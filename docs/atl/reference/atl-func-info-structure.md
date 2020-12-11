---
description: 'Дополнительные сведения: структура _ATL_FUNC_INFO'
title: Структура _ATL_FUNC_INFO
ms.date: 11/04/2016
f1_keywords:
- _ATL_FUNC_INFO
- ATL::_ATL_FUNC_INFO
- ATL._ATL_FUNC_INFO
helpviewer_keywords:
- _ATL_FUNC_INFO structure
- ATL_FUNC_INFO structure
ms.assetid: 441ebe2c-f971-47de-9f52-a258e8d6f88e
ms.openlocfilehash: 6368440347672524bb7d1e3aa3068ef91a2c6f09
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97158859"
---
# <a name="_atl_func_info-structure"></a>Структура _ATL_FUNC_INFO

Содержит сведения о типе, используемые для описания метода или свойства в DISP-интерфейсе.

## <a name="syntax"></a>Синтаксис

```cpp
struct _ATL_FUNC_INFO {
    CALLCONV cc;
    VARTYPE vtReturn;
    SHORT nParams;
    VARTYPE pVarTypes[_ATL_MAX_VARTYPES];
};
```

## <a name="members"></a>Члены

`cc`<br/>
Соглашение о вызовах. При использовании этой структуры с классом [IDispEventSimpleImpl](../../atl/reference/idispeventsimpleimpl-class.md) этот элемент должен быть CC_STDCALL. `CC_CDECL` — единственный вариант, поддерживаемый в Windows CE для `CALLCONV` поля `_ATL_FUNC_INFO` структуры. Любое другое значение не поддерживается, поэтому его поведение не определено.

`vtReturn`<br/>
Тип варианта возвращаемого значения функции.

`nParams`<br/>
Число параметров функции.

`pVarTypes`<br/>
Массив вариативных типов параметров функции.

## <a name="remarks"></a>Комментарии

Внутри библиотека ATL использует эту структуру для хранения информации, полученной из библиотеки типов. Вам может потребоваться манипулировать этой структурой напрямую, если указать сведения о типе для обработчика событий, используемого с классом [IDispEventSimpleImpl](../../atl/reference/idispeventsimpleimpl-class.md) и [SINK_ENTRY_INFO](composite-control-macros.md#sink_entry_info) макросе.

## <a name="example"></a>Пример

При наличии метода disp-интерфейса, определенного в IDL:

[!code-cpp[NVC_ATL_Windowing#139](../../atl/codesnippet/cpp/atl-func-info-structure_1.idl)]

необходимо определить `_ATL_FUNC_INFO` структуру:

[!code-cpp[NVC_ATL_Windowing#140](../../atl/codesnippet/cpp/atl-func-info-structure_2.h)]

## <a name="requirements"></a>Требования

Заголовок: atlcom.h

## <a name="see-also"></a>См. также раздел

[Классы и структуры](../../atl/reference/atl-classes.md)<br/>
[Класс IDispEventSimpleImpl](../../atl/reference/idispeventsimpleimpl-class.md)<br/>
[SINK_ENTRY_INFO](composite-control-macros.md#sink_entry_info)
