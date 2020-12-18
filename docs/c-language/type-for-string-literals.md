---
description: 'Подробнее о следующем: Тип для строковых литералов'
title: Тип для строковых литералов
ms.date: 11/04/2016
helpviewer_keywords:
- string literals, type
- types [C], string literals
ms.assetid: f50a28af-20c1-4440-bdc6-564c86a309c8
ms.openlocfilehash: 9b752d79a1f33e43f24fb86902ba91b3d31777c9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97242825"
---
# <a name="type-for-string-literals"></a>Тип для строковых литералов

Строковые литералы имеют тип массива **`char`** (т. е., **char[ ]** ). (Строки расширенных символов имеют тип массива **`wchar_t`** (т. е., **wchar_t[ ]** ).) Это означает, что строка является массивом с элементами типа **`char`** . Число элементов в массиве равно числу символов в строке плюс один дополнительный элемент для завершающего символа null.

## <a name="see-also"></a>См. также

[Строковые литералы в C](../c-language/c-string-literals.md)
