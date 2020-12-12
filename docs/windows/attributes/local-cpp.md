---
description: 'Дополнительные сведения: local (C++)'
title: Local (атрибут COM C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.local
helpviewer_keywords:
- local attribute
ms.assetid: 35cdd668-bd8e-492a-b7b8-263e7b662437
ms.openlocfilehash: 7fa1366b78576224f8fcc0d91392fe1fc6cb8af9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327514"
---
# <a name="local-c"></a>local (C++)

При использовании в заголовке интерфейса позволяет использовать компилятор MIDL в качестве генератора заголовков. При использовании в отдельной функции обозначает локальную процедуру, для которой заглушки не создаются.

## <a name="syntax"></a>Синтаксис

```cpp
[local]
```

## <a name="remarks"></a>Remarks

**Локальный** атрибут C++ имеет те же функциональные возможности, что и [локальный](/windows/win32/Midl/local) атрибут MIDL.

## <a name="example"></a>Пример

Пример использования **локального** объекта см. в разделе [call_as](call-as.md) .

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|**интерфейс**, метод интерфейса|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|Нет|
|**Недопустимые атрибуты**|`dispinterface`|

Дополнительные сведения см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты IDL](idl-attributes.md)<br/>
[Атрибуты интерфейса](interface-attributes.md)<br/>
[Атрибуты метода](method-attributes.md)<br/>
[call_as](call-as.md)
