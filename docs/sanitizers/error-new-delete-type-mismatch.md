---
title: 'Ошибка: "New-Delete-Type-несоответствие"'
description: Примеры исходного кода и снимки экрана динамической отладки для новых ошибок несоответствия типов удаления.
ms.date: 03/02/2021
f1_keywords:
- new-delete-type-mismatch
helpviewer_keywords:
- new-delete-type-mismatch error
- AddressSanitizer error new-delete-type-mismatch
ms.openlocfilehash: 02ea69b16fbb18878fd46544488ac8f3e0d4e3b5
ms.sourcegitcommit: 6ed44d9c3fb32e965e363b9c69686739a90a2117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "102471130"
---
# <a name="error-new-delete-type-mismatch"></a>Ошибка `new-delete-type-mismatch` (У вызывающей стороны нет прав на запись для ресурса: [subscriptions/])

> Ошибка очистки адреса: размер для освобождения памяти отличается от размера выделения

В этом примере `~Base` вызывается только метод, а не `~Derived` . Компилятор создает вызов, `~Base()` так как `Base` деструктор не является **`virtual`** . При вызове `delete b` деструктор объекта привязывается к определению по умолчанию. Код удаляет пустой базовый класс (или 1 байт в Windows). **`virtual`** Ключевое слово Missing в объявлении деструктора является распространенной ошибкой C++ при использовании наследования.

## <a name="example---virtual-destructor"></a>Пример виртуального деструктора

```cpp
// example1.cpp
// new-delete-type-mismatch error
#include <memory>
#include <vector>

struct T {
    T() : v(100) {}
    std::vector<int> v;
};

struct Base {};

struct Derived : public Base {
    T t;
};

int main() {
    Base *b = new Derived;

    delete b;  // Boom! 

    std::unique_ptr<Base> b1 = std::make_unique<Derived>();

    return 0;
}
```

В базовых классах polybase должны объявляться **`virtual`** деструкторы. Если у класса есть виртуальные функции, он должен иметь виртуальный деструктор.

Чтобы исправить этот пример, добавьте:

```cpp
struct Base {
  virtual ~Base() = default;
}
```

Чтобы выполнить сборку и тестирование этого примера, выполните следующие команды в [командной строке разработчика](../build/building-on-the-command-line.md#developer_command_prompt_shortcuts)Visual Studio 2019 версии 16,9 или более поздней:

```cmd
cl example1.cpp /fsanitize=address /Zi
devenv /debugexe example1.exe
```

### <a name="resulting-error"></a>Итоговая ошибка

:::image type="content" source="media/new-delete-type-mismatch-example-1.png" alt-text="Снимок экрана отладчика, отображающий ошибку несоответствия New-Delete-Type в примере 1.":::

## <a name="see-also"></a>См. также раздел

[Обзор Аддресссанитизер](./asan.md)\
[Известные проблемы Аддресссанитизер](./asan-known-issues.md)\
[Справочник по сборке и языку Аддресссанитизер](./asan-building.md)\
[Справочник по среде выполнения Аддресссанитизер](./asan-runtime.md)\
[Аддресссанитизер теневых байт](./asan-shadow-bytes.md)\
[Аддресссанитизер облачное или распределенное тестирование](./asan-offline-crash-dumps.md)\
[Интеграция отладчика Аддресссанитизер](./asan-debugger-integration.md)\
[Примеры ошибок Аддресссанитизер](./asan-error-examples.md)
