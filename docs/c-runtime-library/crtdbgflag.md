---
description: 'Дополнительные сведения: _crtDbgFlag'
title: _crtDbgFlag
ms.date: 11/04/2016
f1_keywords:
- _crtDbgFlag
- crtDbgFlag
helpviewer_keywords:
- memory allocation, tracking flag
- crtDbgFlag constant
- _crtDbgFlag constant
- debug heap, tracking memory on
- debug heap, control flags
- enable memory allocation tracking flag
- memory, tracking on the debug heap
ms.assetid: 9e7adb47-8ab9-4e19-81d5-e2f237979973
ms.openlocfilehash: ef3c72b89ea9e5e557a567af9a9c52c8e85370ce
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97246769"
---
# <a name="_crtdbgflag"></a>_crtDbgFlag

Флаг **_crtDbgFlag** состоит из пяти битовых полей, которые управляют отслеживанием, проверкой, созданием отчетов и созданием дампа для выделения памяти в отладочной версии кучи. Битовые поля флага задаются с помощью функции [_CrtSetDbgFlag](../c-runtime-library/reference/crtsetdbgflag.md). Этот флаг и его битовые поля объявляются в Crtdbg.h. Этот флаг доступен, только если флаг [_DEBUG](../c-runtime-library/debug.md) был определен в приложении.

Дополнительные сведения об использовании этого флага совместно с другими функциями отладки см. в статье [Функции создания отчетов о состоянии кучи](/visualstudio/debugger/crt-debug-heap-details).

## <a name="see-also"></a>См. также раздел

[Управляющие флаги](../c-runtime-library/control-flags.md)
