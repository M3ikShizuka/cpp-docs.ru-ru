---
description: 'Дополнительные сведения: Math Error M6202'
title: Математическая ошибка M6202
ms.date: 11/04/2016
f1_keywords:
- M6202
helpviewer_keywords:
- M6202
ms.assetid: 4d17045f-c6dc-4705-9512-e9af12c35fb4
ms.openlocfilehash: f6d4c9c8abab59708854eaac6763181018f47473
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97244307"
---
# <a name="math-error-m6202"></a>Математическая ошибка M6202

"функция": ошибка _SING

Аргумент для данной функции был значением для этой функции в единственном числе. Функция не определена для этого аргумента.

Эта ошибка вызывает `_matherr` функцию с именем функции, ее аргументами и типом ошибки. Можно переписать функцию, `_matherr` чтобы настроить обработку определенных математических ошибок с плавающей запятой во время выполнения.
