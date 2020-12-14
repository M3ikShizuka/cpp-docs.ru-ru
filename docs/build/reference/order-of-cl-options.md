---
description: 'Дополнительные сведения: порядок параметров CL'
title: Порядок параметров CL (C++) — Visual Studio
ms.date: 12/14/2018
helpviewer_keywords:
- cl.exe compiler, setting options
ms.assetid: 300908ce-ae00-4b45-964b-e4e69ff6777b
ms.openlocfilehash: bc0290164ff40cf45d8d0a1e9f07e683e408c251
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97226419"
---
# <a name="order-of-cl-options"></a>Порядок параметров CL

Параметры могут находиться в любом месте командной строки CL, за исключением параметра/link, который должен быть последним. Компилятор начинается с параметров, указанных в [переменной среды CL](cl-environment-variables.md) , а затем считывает командную строку слева направо — обрабатывая командные файлы в том порядке, в котором они встречаются. Каждый параметр применяется ко всем файлам в командной строке. Если CL обнаруживает конфликтующие параметры, используется самый правый параметр.

## <a name="see-also"></a>См. также раздел

[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
