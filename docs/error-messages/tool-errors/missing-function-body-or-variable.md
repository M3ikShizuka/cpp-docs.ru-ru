---
description: 'Дополнительные сведения: отсутствует тело функции или переменная'
title: Отсутствует тело функции или переменная
ms.date: 11/04/2016
helpviewer_keywords:
- function body
- variables, missing
ms.assetid: 1a88d809-b14f-46a4-97c4-3e48beb418f2
ms.openlocfilehash: 6a4349c380fc0f573adc8e372f9e4d2fc3f83873
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97155167"
---
# <a name="missing-function-body-or-variable"></a>Отсутствует тело функции или переменная

При использовании только прототипа функции компилятор может продолжить работу без ошибок, но компоновщик не может разрешить вызов адреса, так как код функции или переменное пространство не зарезервировано. Эта ошибка не появится, пока не будет создан вызов функции, которую компоновщик должен разрешить.

## <a name="example-call-to-an-undefined-function"></a>Пример: Вызов неопределенной функции

Вызов функции в Main приведет к возникновению ошибки LNK2019, поскольку прототип позволяет компилятору подумать, что функция существует.  Компоновщик обнаружит, что это не так.

```cpp
// LNK2019_MFBV.cpp
// LNK2019 expected
void DoSomething(void);
int main() {
   DoSomething();
}
```

## <a name="example-call-to-an-implemented-function"></a>Пример: вызов реализованной функции

В C++ Убедитесь, что вы включили реализацию определенной функции для класса, а не только прототипа в определении класса. Если вы определяете класс за пределами файла заголовка, не забудьте включить имя класса перед функцией ( `Classname::memberfunction` ).

```cpp
// LNK2019_MFBV_2.cpp
// LNK2019 expected
struct A {
   static void Test();
};

// Should be void A::Test() {}
void Test() {}

int main() {
   A AObject;
   AObject.Test();
}
```

## <a name="see-also"></a>См. также раздел

[Ошибка средств компоновщика LNK2019](../../error-messages/tool-errors/linker-tools-error-lnk2019.md)
