---
description: Дополнительные сведения о директивах Region и endregion pragma в Microsoft C/C++
title: регион и endregion pragma
ms.date: 01/22/2021
f1_keywords:
- vc-pragma.endregion
- endregion_CPP
- region_CPP
- vc-pragma.region
helpviewer_keywords:
- pragma, region
- pragma, endregion
- endregion pragma
- region pragma
no-loc:
- pragma
ms.openlocfilehash: 68964cd2cab4ff344a8319f970f7ee94be4d378d
ms.sourcegitcommit: a26a66a3cf479e0e827d549a9b850fad99b108d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2021
ms.locfileid: "98713289"
---
# <a name="region-and-endregion-no-locpragma"></a>`region` и `endregion` pragma

`#pragma region` позволяет указать блок кода, который можно развернуть или свернуть при использовании [функции структурирования](/visualstudio/ide/outlining) в редакторе Visual Studio.

## <a name="syntax"></a>Синтаксис

> **`#pragma region`***имя*\
> **`#pragma endregion`***Комментарий*

### <a name="parameters"></a>Параметры

*Метки*\
Используемых Комментарий, отображаемый в редакторе кода.

*безымян*\
Используемых Имя региона. Это имя отображается в редакторе кода.

## <a name="remarks"></a>Примечания

`#pragma endregion` Помечает конец `#pragma region` блока.

`#pragma region`Блок должен заканчиваться `#pragma endregion` директивой.

## <a name="example"></a>Пример

```cpp
// pragma_directives_region.cpp
#pragma region Region_1
void Test() {}
void Test2() {}
void Test3() {}
#pragma endregion Region_1

int main() {}
```

## <a name="see-also"></a>См. также раздел

[Директивы pragma и `__pragma` `_Pragma` Ключевые слова и](./pragma-directives-and-the-pragma-keyword.md)
