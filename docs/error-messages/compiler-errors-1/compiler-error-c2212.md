---
description: 'Дополнительные сведения о: Ошибка компилятора C2212'
title: Ошибка компилятора C2212
ms.date: 11/04/2016
f1_keywords:
- C2212
helpviewer_keywords:
- C2212
ms.assetid: 3fdab304-272c-4d07-bfd4-fad75170e536
ms.openlocfilehash: 614c93cf2c933cbdf043108c35bc06260a123ce1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97245607"
---
# <a name="compiler-error-c2212"></a>Ошибка компилятора C2212

"идентификатор": __based недоступен для указателей на функции

Указатели на функции не могут быть объявлены **`__based`** . Если требуются данные на основе кода, используйте **`__declspec`** ключевое слово или `data_seg` директиву pragma.
