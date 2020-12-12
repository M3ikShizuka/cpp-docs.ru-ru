---
description: 'Дополнительные сведения о: Ошибка компилятора C2129'
title: Ошибка компилятора C2129
ms.date: 11/04/2016
f1_keywords:
- C2129
helpviewer_keywords:
- C2129
ms.assetid: 21a8223e-1d22-4baa-9ca1-922b7f751dd0
ms.openlocfilehash: 5efb19aa3f4edd14dd6cfab93c3880745b08e59d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323159"
---
# <a name="compiler-error-c2129"></a>Ошибка компилятора C2129

статическая функция "функция" объявлена, но не определена

В **`static`** функцию, которая не определена, делается прямая ссылка.

**`static`** Функция должна быть определена в области файла. Если функция определена в другом файле, она должна быть объявлена **`extern`** .
