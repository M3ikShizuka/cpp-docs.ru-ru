---
description: 'Дополнительные сведения: псевдоним'
title: ALIAS (MASM)
ms.date: 12/17/2019
f1_keywords:
- Alias
helpviewer_keywords:
- ALIAS directive
ms.assetid: d9725c49-58de-41da-ab01-b06a56cf5cf2
ms.openlocfilehash: 7d5072cec8ef56f3dd2202617b3274c958a25d66
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97121762"
---
# <a name="alias"></a>ALIAS

Директива **Alias** создает альтернативное имя для функции.  Это позволяет создать несколько имен для функции или создать библиотеки, позволяющие компоновщику (LINK.exe) сопоставлять старую функцию с новой функцией.

## <a name="syntax"></a>Синтаксис

> **ПСЕВДОНИМ \<**_alias_**> = \<**_actual-name_**>**

#### <a name="parameters"></a>Параметры

*фактическое имя*\
Фактическое имя функции или процедуры.  Угловые скобки являются обязательными.

*псевдоним*\
Альтернативное или имя псевдонима.  Угловые скобки являются обязательными.

## <a name="see-also"></a>См. также раздел

[Справочник по директивам](directives-reference.md)\
[Грамматика MASM BNF](masm-bnf-grammar.md)
