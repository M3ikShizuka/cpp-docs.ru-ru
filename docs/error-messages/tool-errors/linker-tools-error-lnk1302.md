---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK1302'
title: Ошибка средств компоновщика LNK1302
ms.date: 11/04/2016
f1_keywords:
- LNK1302
helpviewer_keywords:
- LNK1302
ms.assetid: aea3c753-c2c4-4249-bbc3-f2d4f0164b5e
ms.openlocfilehash: 33e9a406cde7910c7340fdfe256711c47eee45cf
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97193699"
---
# <a name="linker-tools-error-lnk1302"></a>Ошибка средств компоновщика LNK1302

поддерживаются только ссылки на надежные. netmodule. не удается связать файл. netmodule

NETMODULE-код (скомпилированный с параметром **/LN**) был передан компоновщику при попытке вызвать компоновку MSIL.  Модуль C++ является допустимым для компоновки MSIL, если он компилируется с **/clr: Сейф**.

Чтобы исправить эту ошибку, Скомпилируйте с **параметром/clr: Сейф** , чтобы включить компоновку MSIL, или передайте компоновщику вместо модуля файл **/CLR** или **/clr: pure** . obj.

Дополнительные сведения см. в разделе

- [/LN (создание модуля MSIL)](../../build/reference/ln-create-msil-module.md)

- [Файлы NETMODULE в качестве входных файлов компоновщика](../../build/reference/netmodule-files-as-linker-input.md)
