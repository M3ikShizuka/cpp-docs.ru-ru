---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK1223'
title: Ошибка средств компоновщика LNK1223
ms.date: 11/04/2016
f1_keywords:
- LNK1223
helpviewer_keywords:
- LNK1223
ms.assetid: c4728c36-daee-462f-a1c7-8733dcdec88e
ms.openlocfilehash: eb1937f253d324781834d0b6f465c79f7009787f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97194063"
---
# <a name="linker-tools-error-lnk1223"></a>Ошибка средств компоновщика LNK1223

недопустимый или поврежденный файл: файл содержит недопустимые фрагменты .pdata

Для RISC-платформ, использующих pdata, эта ошибка возникнет, если компилятор выдаст фрагмент .pdata с несортированными записями.

Чтобы устранить эту проблему, попробуйте выполнить компиляцию без включения [/GL (оптимизация всей программы)](../../error-messages/tool-errors/linker-tools-error-lnk1223.md) . Также в некоторых случаях эта ошибка может возникнуть из-за пустого текста функций.
