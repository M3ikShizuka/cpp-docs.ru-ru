---
description: 'Дополнительные сведения о: Неустранимая ошибка C1081'
title: Неустранимая ошибка C1081
ms.date: 11/04/2016
f1_keywords:
- C1081
helpviewer_keywords:
- C1081
ms.assetid: e58adf17-cbe1-4955-a5c7-80622bbba249
ms.openlocfilehash: 97e1070cb24a70750e9c7d9f78a3860b26a7831a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330700"
---
# <a name="fatal-error-c1081"></a>Неустранимая ошибка C1081

"символ": слишком длинное имя файла

Длина пути к файлу превышает длину `_MAX_PATH` (определяется в STDLIB. h как 260 символов). Сократите имя файла.

При вызове CL.exe с коротким именем файла компилятору может потребоваться создать полный путь. Например, `cl -c myfile.cpp` может привести к тому, что компилятор создаст:

```
D:\<very-long-directory-path>\myfile.cpp
```
