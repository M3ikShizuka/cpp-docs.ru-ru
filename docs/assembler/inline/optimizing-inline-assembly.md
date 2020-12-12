---
description: 'Дополнительные сведения: оптимизация встроенной сборки'
title: Оптимизация встроенного кода на языке ассемблера
ms.date: 08/30/2018
helpviewer_keywords:
- storage, optimizing in inline assembly
- optimization, inline assembly
- inline assembly, optimizing
- optimizing performance, inline assembly
- __asm keyword [C++], optimizing
ms.assetid: 52a7ec83-9782-4d96-94c1-53bb2ac9e8c8
ms.openlocfilehash: 62c4dad85128089cdcf85f4156884747f928338f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97122100"
---
# <a name="optimizing-inline-assembly"></a>Оптимизация встроенного кода на языке ассемблера

**Блок, относящийся только к системам Microsoft**

Наличие **`__asm`** блока в функции влияет на оптимизацию несколькими способами. Во первых, компилятор не пытается оптимизировать **`__asm`** сам блок. То, что написано на языке ассемблера, то и получается. Во вторых, присутствие **`__asm`** блока влияет на регистрацию переменного хранилища. Компилятор позволяет избежать регистрирует переменных в **`__asm`** блоке, если содержимое регистра будет изменено **`__asm`** блоком. Наконец, включение языка ассемблера в функцию затрагивает некоторые другие аспекты оптимизации уровня функции.

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Встроенный ассемблер](../../assembler/inline/inline-assembler.md)<br/>
