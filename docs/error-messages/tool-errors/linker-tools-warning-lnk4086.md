---
description: 'Дополнительные сведения: Предупреждение средств компоновщика LNK4086'
title: Предупреждение средств компоновщика LNK4086
ms.date: 11/04/2016
f1_keywords:
- LNK4086
helpviewer_keywords:
- LNK4086
ms.assetid: ea1eecbb-ba2c-41bb-9a4f-fa0808a4b92d
ms.openlocfilehash: f19138d895706579cff13bd1d43b9a64ccaa5044
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97210118"
---
# <a name="linker-tools-warning-lnk4086"></a>Предупреждение средств компоновщика LNK4086

точка входа "функция" не __stdcall с числом байтов аргументов; образ не может быть запущен

Точка входа для библиотеки DLL должна иметь значение **`__stdcall`** . Либо перекомпилируйте функцию с параметром [/gz](../../build/reference/gd-gr-gv-gz-calling-convention.md) , либо укажите **`__stdcall`** или WINAPI при определении функции.
