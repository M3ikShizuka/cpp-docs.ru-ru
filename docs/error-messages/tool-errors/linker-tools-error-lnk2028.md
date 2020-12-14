---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK2028'
title: Ошибка средств компоновщика LNK2028
ms.date: 11/04/2016
f1_keywords:
- LNK2028
helpviewer_keywords:
- LNK2028
ms.assetid: e2b03293-6066-464d-a050-ce747bcf7f0e
ms.openlocfilehash: 31b20cc572a44b1260f58eb03519b60050c0246c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97275728"
---
# <a name="linker-tools-error-lnk2028"></a>Ошибка средств компоновщика LNK2028

"*exported_function*" (*decorated_name*), на который указывает ссылка в функции "*function_containing_function_call*" (*decorated_name*)

## <a name="remarks"></a>Комментарии

При попытке импортировать собственную функцию в чистый образ Помните, что неявные соглашения о вызовах отличаются от собственных и чистых компиляций.

Параметр компилятора **/clr: pure** является устаревшим в visual Studio 2015 и не поддерживается в visual Studio 2017.

## <a name="examples"></a>Примеры

Этот пример кода создает компонент с экспортированной собственной функцией, соглашение о вызовах которого неявно [__cdecl](../../cpp/cdecl.md).

```cpp
// LNK2028.cpp
// compile with: /LD
__declspec(dllexport) int func() {
   return 3;
}
```

В следующем примере создается чистый клиент, использующий собственную функцию. Однако соглашение о вызовах в **/clr: pure** [__clrcall](../../cpp/clrcall.md). Следующий пример приводит к возникновению ошибки LNK2028.

```cpp
// LNK2028_b.cpp
// compile with: /clr:pure lnk2028.lib
// LNK2028 expected
int func();

int main() {
   return func();
}
```
