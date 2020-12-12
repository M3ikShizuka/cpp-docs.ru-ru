---
description: Дополнительные сведения см. в статье ссылки на сегменты во встроенном коде на языке ассемблера
title: Ссылки на сегменты во встроенном коде на языке ассемблера
ms.date: 08/30/2018
helpviewer_keywords:
- references, inline assembly
- segment references in inline assembly
- inline assembly, segment references
- registers
- inline assembly, registers
- registers, inline assembly
ms.assetid: c63e6bb4-49d9-4fa1-bb22-eea21b5cbc0f
ms.openlocfilehash: 9f9f37d7c45700358cc958f12d6f2d97da6bcf01
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97122087"
---
# <a name="segment-references-in-inline-assembly"></a>Ссылки на сегменты во встроенном коде на языке ассемблера

**Блок, относящийся только к системам Microsoft**

Ссылаться на сегменты следует по регистру, а не по имени (например, имя сегмента `_TEXT` недопустимо). В переопределениях сегментов необходимо явно использовать регистр, как в ES:[BX].

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Использование языка ассемблера в блоках __asm](../../assembler/inline/using-assembly-language-in-asm-blocks.md)<br/>
