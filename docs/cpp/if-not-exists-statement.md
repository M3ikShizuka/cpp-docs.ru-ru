---
description: 'Дополнительные сведения о инструкции: __if_not_exists'
title: Оператор __if_not_exists
ms.date: 11/04/2016
f1_keywords:
- __if_not_exists_cpp
helpviewer_keywords:
- __if_not_exists keyword [C++]
ms.assetid: a2f322d4-e96f-4a32-954e-4323d20c6e32
ms.openlocfilehash: 29f98c2d07858077207c10dfcdd45b9ce51268e7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97113952"
---
# <a name="__if_not_exists-statement"></a>Оператор __if_not_exists

**`__if_not_exists`** Оператор проверяет, существует ли указанный идентификатор. Если идентификатор не существует, выполняется определенный блок операторов.

## <a name="syntax"></a>Синтаксис

```
__if_not_exists ( identifier ) {
statements
};
```

#### <a name="parameters"></a>Параметры

*identifier*\
Идентификатор, наличие которого требуется проверить.

*инструкции*\
Одна или несколько инструкций для выполнения, если *идентификатор* не существует.

## <a name="remarks"></a>Комментарии

> [!CAUTION]
> Для достижения наиболее достоверных результатов используйте **`__if_not_exists`** инструкцию под следующими ограничениями.

- Примените **`__if_not_exists`** инструкцию только к простым типам, а не к шаблонам.

- Примените **`__if_not_exists`** инструкцию к идентификаторам как внутри, так и вне класса. Не применяйте **`__if_not_exists`** инструкцию к локальным переменным.

- Используйте **`__if_not_exists`** оператор только в теле функции. За пределами тела функции **`__if_not_exists`** инструкция может проверять только полностью определенные типы.

- При проверке перегруженных функций невозможно выполнить проверку определенной формы перегрузки.

Дополнение к **`__if_not_exists`** оператору является оператором [__if_exists](../cpp/if-exists-statement.md) .

## <a name="example"></a>Пример

Пример использования см **`__if_not_exists`** . в разделе [оператор __if_exists](../cpp/if-exists-statement.md).

## <a name="see-also"></a>См. также раздел

[Инструкции выбора](../cpp/selection-statements-cpp.md)<br/>
[Ключевые слова](../cpp/keywords-cpp.md)<br/>
[__if_exists, инструкция](../cpp/if-exists-statement.md)
