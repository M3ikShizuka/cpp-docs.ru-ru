---
description: 'Дополнительные сведения о: importlib'
title: importlib (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.importlib
helpviewer_keywords:
- importlib attribute
ms.assetid: f129e459-b8d3-4aca-a0bc-ee53e18b62ed
ms.openlocfilehash: f3000be3415ed944d621ebcd36442e33951efc84
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97114953"
---
# <a name="importlib"></a>importlib

Делает типы, которые уже были скомпилированы в другую библиотеку типов, доступными для создаваемой библиотеки типов.

## <a name="syntax"></a>Синтаксис

```cpp
[ importlib("tlb_file") ];
```

### <a name="parameters"></a>Параметры

*tlb_file*<br/>
Заключенное в кавычки имя TLB-файла, который необходимо импортировать в библиотеку типов текущего проекта.

## <a name="remarks"></a>Комментарии

Атрибут **importlib** C++ вызывает `importlib` помещение инструкции в блок библиотеки созданного idl-файла. Атрибут **importlib** имеет те же функциональные возможности, что и атрибут [importlib](/windows/win32/Midl/importlib) MIDL.

## <a name="example"></a>Пример

В следующем коде показан пример использования **importlib**:

```cpp
// cpp_attr_ref_importlib.cpp
// compile with: /LD
[module(name="MyLib")];
[importlib("importlib.tlb")];
```

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|В любом месте|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты компилятора](compiler-attributes.md)<br/>
[Изолированные атрибуты](stand-alone-attributes.md)<br/>
[import](import.md)<br/>
[importidl](importidl.md)<br/>
[относится](include-cpp.md)<br/>
[инклуделиб](includelib-cpp.md)
