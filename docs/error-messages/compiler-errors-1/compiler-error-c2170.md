---
description: 'Дополнительные сведения о: Ошибка компилятора C2170'
title: Ошибка компилятора C2170
ms.date: 11/04/2016
f1_keywords:
- C2170
helpviewer_keywords:
- C2170
ms.assetid: d5c663f0-2459-4e11-a8bf-a52b62f3c71d
ms.openlocfilehash: 2f6093221d214aa12f6b90f40dde14518e44e08e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97322262"
---
# <a name="compiler-error-c2170"></a>Ошибка компилятора C2170

"идентификатор": не объявлен как функция, не может быть встроенным

### <a name="to-fix-by-checking-the-following-possible-causes"></a>Чтобы устранить ошибку, проверьте указанные ниже возможные причины ее возникновения.

1. Директива pragma `intrinsic` используется для элемента, отличного от функции.

1. Директива pragma `intrinsic` используется для функции без встроенной формы.
