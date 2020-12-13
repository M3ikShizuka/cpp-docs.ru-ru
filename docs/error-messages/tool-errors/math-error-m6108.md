---
description: 'Дополнительные сведения: Math Error M6108'
title: Математическая ошибка M6108
ms.date: 11/04/2016
f1_keywords:
- M6108
helpviewer_keywords:
- M6108
ms.assetid: 054893b4-49bc-45d9-882f-7cb50ba387c0
ms.openlocfilehash: 1a0acf13bd166e499334cb13de33093c2c804f5f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97143888"
---
# <a name="math-error-m6108"></a>Математическая ошибка M6108

квадратный корень

Операнд в операции с квадратным корнем был отрицательным.

Программа завершается с кодом выхода 136.

> [!NOTE]
> `sqrt`Функция в библиотеке времени выполнения C и встроенная функция Fortran **sqrt** не создают эту ошибку. Функция C `sqrt` проверяет аргумент перед выполнением операции и возвращает значение ошибки, если операнд является отрицательным. Функция FORTRAN **sqrt** создает ошибку домена [M6201](../../error-messages/tool-errors/math-error-m6201.md) , а не эту ошибку.
