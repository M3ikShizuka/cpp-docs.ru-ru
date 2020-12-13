---
description: 'Дополнительные сведения о: Ошибка компилятора C3201'
title: Ошибка компилятора C3201
ms.date: 11/04/2016
f1_keywords:
- C3201
helpviewer_keywords:
- C3201
ms.assetid: ec19cd64-1789-40a3-b2db-dff2852b9d98
ms.openlocfilehash: 3cd6e037cd9dbb0638040e2f3eca61dab1dabb46
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330643"
---
# <a name="compiler-error-c3201"></a>Ошибка компилятора C3201

список параметров шаблона для класса-шаблона template не совпадает со списком параметров шаблона для параметра шаблона template

Вы передали шаблон класса в аргументе шаблону класса, не принимающему параметр шаблона, или вы передали несоответствующее число аргументов шаблона для аргумента шаблона по умолчанию.

```cpp
// C3201.cpp
template<typename T1, typename T2>
class X1
{
};

template<template<typename T> class U = X1>   // C3201
class X2
{
};

template<template<typename T, typename V> class U = X1>   // OK
class X3
{
};
```
