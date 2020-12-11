---
description: 'Дополнительные сведения: доступ к членам'
title: Доступ к членам
ms.date: 11/04/2016
helpviewer_keywords:
- member-selection operators [C++]
- pointers, smart
- member access, overloaded operators
- operator overloading [C++], member access operators
- smart pointers, definition
- smart pointers
ms.assetid: 8c7b2c43-eb92-4d42-9a8e-61aa37d71333
ms.openlocfilehash: c35eb2e7e24da9f8e8988b47ebfd8a59df815cee
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97161719"
---
# <a name="member-access"></a>Доступ к членам

Доступ к членам класса можно контролировать путем перегрузки оператора доступа к членам ( **->** ). В данном случае этот оператор считается унарным оператором, и функция перегруженного оператора должна быть функцией-членом класса. Поэтому объявление такой функции выглядит следующим образом.

## <a name="syntax"></a>Синтаксис

```
class-type *operator->()
```

## <a name="remarks"></a>Remarks

где *Class-Type* — это имя класса, к которому принадлежит этот оператор. Функция оператора доступа к члену должна быть нестатической функцией-членом.

Этот оператор используется (часто вместе с оператором разыменования указателя) для реализации интеллектуальных указателей, которые проверяют указатели до разыменования или подсчета.

Языковой элемент **.** оператор доступа к членам не может быть перегружен.

## <a name="see-also"></a>См. также раздел

[Перегрузка операторов](../cpp/operator-overloading.md)
