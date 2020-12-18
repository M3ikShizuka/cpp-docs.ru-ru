---
description: 'Подробнее о следующем: Функции Naked'
title: Функции Naked
ms.date: 11/04/2016
helpviewer_keywords:
- naked functions
- functions [C++], naked
- prolog code
- epilog code
ms.assetid: 2543c8af-00d4-4a2a-8a87-e746da1f9929
ms.openlocfilehash: 1cea9bf2497a14bc7007f97b2c3db68eafc15059
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97243358"
---
# <a name="naked-functions"></a>Функции Naked

**Блок, относящийся только к системам Microsoft**

Атрибут класса хранения `naked` является расширением языка C для систем Microsoft. Код функций, объявленных с атрибутом `naked`, создается компилятором без кода пролога и эпилога. Эту возможность можно использовать, чтобы создавать свой собственный код на языке ассемблера и вставлять его в качестве пролога и эпилога. Функции с атрибутом naked особенно полезны для написания драйверов виртуальных устройств.

Поскольку атрибут `naked` относится только к определению функции и не является модификатором типа, в функциях с этим атрибутом используется расширенный синтаксис атрибутов, который описывается в статье [Расширенные атрибуты классов хранения в C](../c-language/c-extended-storage-class-attributes.md).

В следующем примере определяется функция с атрибутом `naked`.

```
__declspec( naked ) int func( formal_parameters )
{
   /* Function body */
}
```

Другой пример:

```
#define Naked   __declspec( naked )

Naked int func( formal_parameters )
{
   /* Function body */
}
```

Атрибут `naked` влияет только на создание кода компилятора для последовательностей пролога и эпилога функции. Код, который создается для вызова таких функций, не зависит от этого атрибута. Таким образом, атрибут `naked` не входит в тип функции, а указатели на функции не могут иметь атрибут `naked`. Кроме того, атрибут `naked` не может применяться к определениям данных. Например, следующий код вызывает ошибки:

```
__declspec( naked ) int i;  /* Error--naked attribute not */
                            /* permitted on data declarations. */
```

Атрибут `naked` относится только к определению функции и не может быть определен в прототипе функции. Следующее объявление создает ошибку компилятора:

```
__declspec( naked ) int func();   /* Error--naked attribute not */
                     /* permitted on function declarations.    */   \
```

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Определения функций в C](../c-language/c-function-definitions.md)
