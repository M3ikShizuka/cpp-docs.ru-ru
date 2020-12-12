---
description: 'Подробнее о: Region, endregion прагмы'
title: Директивы pragma region, endregion
ms.date: 08/29/2019
f1_keywords:
- vc-pragma.endregion
- endregion_CPP
- region_CPP
- vc-pragma.region
helpviewer_keywords:
- pragmas, region
- pragmas, endregion
- endregion pragma
- region pragma
ms.assetid: c697f807-622f-4796-851b-68a42bbecd84
ms.openlocfilehash: a12305240f0c05913d16c5f26fb64661fc08e736
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97167426"
---
# <a name="region-endregion-pragmas"></a>Директивы pragma region, endregion

`#pragma region` позволяет указать блок кода, который можно развернуть или свернуть при использовании [функции структурирования](/visualstudio/ide/outlining) в редакторе Visual Studio Code.

## <a name="syntax"></a>Синтаксис

> *имя* **региона #pragma**\
> **#pragma** *Комментарий* endregion

### <a name="parameters"></a>Параметры

*Метки*\
Используемых Комментарий, отображаемый в редакторе кода.

*безымян*\
Используемых Имя региона. Это имя отображается в редакторе кода.

## <a name="remarks"></a>Комментарии

`#pragma endregion` Помечает конец `#pragma region` блока.

`#region`Блок должен заканчиваться `#pragma endregion` директивой.

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

[Директивы pragma и ключевое слово __pragma](../preprocessor/pragma-directives-and-the-pragma-keyword.md)
