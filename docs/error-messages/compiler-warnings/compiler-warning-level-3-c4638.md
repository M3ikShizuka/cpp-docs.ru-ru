---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4638'
title: Предупреждение компилятора (уровень 3) C4638
ms.date: 08/27/2018
f1_keywords:
- C4638
helpviewer_keywords:
- C4638
ms.assetid: 2c07923a-e103-4e40-bd11-fdfed428a5ec
ms.openlocfilehash: fc771004ebbfeef436a456523e2e2fc87382a291
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338560"
---
# <a name="compiler-warning-level-3-c4638"></a>Предупреждение компилятора (уровень 3) C4638

> Целевой комментарий XML-документа: ссылка на неизвестный символ "*символ*"

## <a name="remarks"></a>Комментарии

Компилятору не удалось разрешить символ (*символ*). Символ должен быть допустимым при компиляции.

## <a name="example"></a>Пример

В следующем примере возникает ошибка C4638.

```cpp
// C4638.cpp
// compile with: /clr /doc /LD /W3
using namespace System;

/// Text for class MyClass.
public ref class MyClass {
public:
   /// <summary> Text </summary>
   /// <see cref="aSymbolThatAppearsNowhereInMyProject"/>
   // Try the following line instead:
   // /// <see cref="System::Console::WriteLine"/>
   void MyMethod() {}
};   // C4638
```
