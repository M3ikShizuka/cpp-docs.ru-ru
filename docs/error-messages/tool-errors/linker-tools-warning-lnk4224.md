---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4224'
title: Предупреждение средств компоновщика LNK4224
ms.date: 11/04/2016
f1_keywords:
- LNK4224
helpviewer_keywords:
- LNK4224
ms.assetid: 8624b70e-0b93-43cf-b457-834d38632d0b
ms.openlocfilehash: 35cae5c46b91493a40d4d52650f781010f6d6379
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327910"
---
# <a name="linker-tools-warning-lnk4224"></a>Предупреждение средств компоновщика LNK4224

> *параметр* больше не поддерживается; игнорируют

## <a name="remarks"></a>Комментарии

Указан недопустимый устаревший параметр компоновщика, который не учитывается.

Например, LNK4224 может возникать, если в OBJ-файле присутствует директива/Comment. Директива/Comment была бы добавлена с помощью директивы pragma [comment (C/C++)](../../preprocessor/comment-c-cpp.md) с использованием нерекомендуемого параметра exestr. Используйте DUMPBIN [/ALL](../../build/reference/all.md) для просмотра директив компоновщика в OBJ-файле.

По возможности измените источник для obj и удалите директиву pragma. Если пропустить это предупреждение, возможно, исполняемый файл, скомпилированный с **параметром/clr: pure** , не будет выполняться должным образом. Параметр компилятора **/clr: pure** является устаревшим в visual Studio 2015 и не поддерживается в visual Studio 2017.

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки LNK4224.

```cpp
// LNK4224.cpp
// compile with: /c /Zi
// post-build command: link LNK4224.obj /debug /debugtype:map
int main () {
   return 0;
}
```
