---
description: 'Дополнительные сведения о: Неустранимая ошибка C1091'
title: Неустранимая ошибка C1091
ms.date: 11/04/2016
f1_keywords:
- C1091
helpviewer_keywords:
- C1091
ms.assetid: 812d4201-9154-48b0-b9af-5959c082ca33
ms.openlocfilehash: 3863600e10dcfbef274424559e2cda0ca791406b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97145175"
---
# <a name="fatal-error-c1091"></a>Неустранимая ошибка C1091

ограничение компилятора: длина строки превышает "длину" байт

Длина строковой константы превышает установленное ограничение.

Можно разбить статическую строку на две (или более) переменных и использовать функцию [strcpy_s](../../c-runtime-library/reference/strcpy-s-wcscpy-s-mbscpy-s.md) для объединения результатов в объявлении или во время выполнения.
