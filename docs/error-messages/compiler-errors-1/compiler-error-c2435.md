---
description: 'Дополнительные сведения о: Ошибка компилятора C2435'
title: Ошибка компилятора C2435
ms.date: 11/04/2016
f1_keywords:
- C2435
helpviewer_keywords:
- C2435
ms.assetid: be6aa8f8-579b-42ea-bdd8-2d01393646ad
ms.openlocfilehash: d0ab5d8c7c45c9636a5e48acc17d3ac379c755a9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97189942"
---
# <a name="compiler-error-c2435"></a>Ошибка компилятора C2435

> "*var*": для динамической инициализации требуется управляемый CRT, не удается выполнить компиляцию с/CLR: Сейф

## <a name="remarks"></a>Комментарии

Параметры компилятора **/clr: pure** и **/clr: Сейф** являются устаревшими в Visual Studio 2015 и не поддерживаются в Visual Studio 2017.

Инициализация глобальной переменной домена для каждого приложения требует компиляции CRT с параметром `/clr:pure` , который не создает проверяемый образ.

Дополнительные сведения см. в разделах [appdomain](../../cpp/appdomain.md) и [process](../../cpp/process.md).

## <a name="example"></a>Пример

Следующий пример приводит к возникновению ошибки C2435:

```cpp
// C2435.cpp
// compile with: /clr:safe /c
int globalvar = 0;   // C2435

__declspec(process)
int globalvar2 = 0;
```
