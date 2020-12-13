---
description: 'Дополнительные сведения о: Ошибка компилятора C2856'
title: Ошибка компилятора C2856
ms.date: 11/04/2016
f1_keywords:
- C2856
helpviewer_keywords:
- C2856
ms.assetid: fe616c51-124e-49e3-9dd8-883ec1660680
ms.openlocfilehash: 8594bc5902e13967084aa3695131d616a4cf04da
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97337557"
---
# <a name="compiler-error-c2856"></a>Ошибка компилятора C2856

\#Директива pragma hdrstop не может находиться в блоке #if

`hdrstop`Директиву pragma нельзя поместить в тело блока условной компиляции.

Переместите `#pragma hdrstop` оператор в область, которая не содержится в `#if/#endif` блоке.
