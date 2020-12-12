---
description: 'Дополнительные сведения: Неустранимая ошибка компилятора ресурсов RW1025'
title: Неустранимая ошибка компилятора ресурсов RW1025
ms.date: 11/04/2016
f1_keywords:
- RW1025
helpviewer_keywords:
- RW1025
ms.assetid: 561a02af-e7e0-442a-8ad3-a00b2ca1b62e
ms.openlocfilehash: 40404f8d6dc16b73f93255a18ce8c632cc1e014a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97237196"
---
# <a name="resource-compiler-fatal-error-rw1025"></a>Неустранимая ошибка компилятора ресурсов RW1025

Недостаточно памяти в куче

Проверьте наличие в памяти резидентного программного обеспечения, которое может занимать слишком много пространства. Используйте программу CHKDSK для определения объема используемой памяти.

При создании большого файла ресурсов разделите сценарий ресурсов на два файла. После создания двух RES файлов используйте командную строку MS-DOS, чтобы объединить их вместе:

```
copy first.res /b + second.res /b full.res
```
