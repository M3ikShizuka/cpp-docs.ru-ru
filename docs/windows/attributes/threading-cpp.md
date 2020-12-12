---
description: 'Дополнительные сведения: работа с потоками (C++)'
title: Создание потоков (атрибут COM в C++)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.threading
helpviewer_keywords:
- threading attribute
ms.assetid: 9b558cd6-fbf0-4602-aed5-31c068550ce3
ms.openlocfilehash: e46a3720280fe7ee7b9debae98e3270825e8db40
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327247"
---
# <a name="threading-c"></a>threading (C++)

Указывает потоковую модель для COM-объекта.

## <a name="syntax"></a>Синтаксис

```cpp
[ threading(model=enumeration) ]
```

### <a name="parameters"></a>Параметры

*model*<br/>
Используемых Одна из следующих потоков моделей:

- `apartment` (потоковое разделение)

- `neutral` (.NET Framework компонентов без пользовательского интерфейса)

- `single` (простая организация потоков)

- `free` (свободная организация)

- `both` (потоковая подразделение и свободная организация)

Значение по умолчанию — `apartment`.

## <a name="remarks"></a>Примечания

Атрибут **Threading** C++ не отображается в созданном IDL-файле, но будет использоваться в реализации объекта COM.

В проектах ATL, если имеется также атрибут [coclass](coclass.md) , потоковая модель, заданная *моделью* , передается в качестве параметра шаблона в класс [CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md) , который вставляется `coclass` атрибутом.

Атрибут **потоковой обработки** также защищает доступ к [event_source](event-source.md).

## <a name="example"></a>Пример

Пример использования **потоков** см. в примере с [лицензией](licensed.md) .

## <a name="requirements"></a>Требования

| Контекст атрибута | Значение |
|-|-|
|**Относится к**|**`class`**, **`struct`**|
|**REPEATABLE**|Нет|
|**Требуемые атрибуты**|**кокласс**|
|**Недопустимые атрибуты**|Нет|

Дополнительные сведения о контекстах атрибутов см. в разделе [Контексты атрибутов](cpp-attributes-com-net.md#contexts).

## <a name="see-also"></a>См. также раздел

[Атрибуты COM](com-attributes.md)<br/>
[Атрибуты typedef, enum, Union и struct](typedef-enum-union-and-struct-attributes.md)<br/>
[Атрибуты класса](class-attributes.md)<br/>
[Поддержка многопоточности для устаревшего кода (Visual C++)](../../parallel/multithreading-support-for-older-code-visual-cpp.md)<br/>
[Нейтральные подразделения](/windows/win32/cossdk/neutral-apartments)
