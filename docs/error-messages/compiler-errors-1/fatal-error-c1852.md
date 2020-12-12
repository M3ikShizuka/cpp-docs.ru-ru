---
description: 'Дополнительные сведения о: Неустранимая ошибка C1852'
title: Неустранимая ошибка C1852
ms.date: 11/04/2016
f1_keywords:
- C1852
helpviewer_keywords:
- C1852
ms.assetid: fa011004-b8d6-46f1-ba80-4785e4ce137f
ms.openlocfilehash: 0b4976566b8101ecd4f35d20854ef6124a15246e
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97276248"
---
# <a name="fatal-error-c1852"></a>Неустранимая ошибка C1852

"имя_файла" не является допустимым файлом предкомпилированного заголовка

Файл не является предкомпилированным заголовком.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>Чтобы устранить ошибку, проверьте указанные ниже возможные причины ее возникновения.

1. Указан недопустимый файл с **/Yu** или **#pragma hdrstop**.

1. Если не указано иное, компилятор предполагает расширение файла PCH.
