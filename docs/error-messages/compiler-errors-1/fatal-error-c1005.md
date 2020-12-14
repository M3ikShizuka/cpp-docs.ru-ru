---
description: 'Дополнительные сведения о: Неустранимая ошибка C1005'
title: Неустранимая ошибка C1005
ms.date: 11/04/2016
f1_keywords:
- C1005
helpviewer_keywords:
- C1005
ms.assetid: 150daf8e-a38a-4669-9c1a-a05b5a1f65ef
ms.openlocfilehash: c57856a09aa3473c7f5ba3049a2962fb4553e4e5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97262676"
---
# <a name="fatal-error-c1005"></a>Неустранимая ошибка C1005

слишком большая строка для буфера

Строка в промежуточном файле компилятора вызвала переполнение буфера.

Эта ошибка может возникнуть, если размер параметра, передаваемого в параметр компилятора [/Fd](../../build/reference/fd-program-database-file-name.md) или [/Yl](../../build/reference/yl-inject-pch-reference-for-debug-library.md) , превышает 256 байт.
