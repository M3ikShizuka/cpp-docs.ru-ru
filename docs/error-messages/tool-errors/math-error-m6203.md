---
description: 'Дополнительные сведения: Math Error M6203'
title: Математическая ошибка M6203
ms.date: 11/04/2016
f1_keywords:
- M6203
helpviewer_keywords:
- M6203
ms.assetid: bd7fdd1c-83e4-4d6a-901e-10a0308bf5be
ms.openlocfilehash: fcb123af8c79b5ce839e13247f59cbbed42736f4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97143875"
---
# <a name="math-error-m6203"></a>Математическая ошибка M6203

"функция": ошибка _OVERFLOW

Указанный результат функции слишком велик для представления.

Эта ошибка вызывает `_matherr` функцию с именем функции, ее аргументами и типом ошибки. Можно переписать функцию, `_matherr` чтобы настроить обработку определенных математических ошибок с плавающей запятой во время выполнения.
