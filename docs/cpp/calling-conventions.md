---
description: 'Дополнительные сведения: соглашения о вызовах'
title: Соглашения о вызовах
ms.date: 11/04/2016
helpviewer_keywords:
- calling conventions
ms.assetid: 11b1e45c-8fd1-420b-bca0-a19e294c1d85
ms.openlocfilehash: bb5dab14e9d046b6ccee75a4fb37bd7b105902dc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97308657"
---
# <a name="calling-conventions"></a>Соглашения о вызовах

В компиляторе Visual C/C++ принято несколько разных соглашений о вызовах внутренних и внешних функций. Зная эти подходы, вам будет проще выполнять отладку программ и привязывать свой код к процедурам на языке ассемблера.

В разделах, посвященных этой теме, говорится о том, чем различаются эти соглашения о вызовах, как передаются аргументы и как функции возвращают значения. Кроме того, в них рассматриваются вызовы возможностей с атрибутом naked — дополнительная возможность, благодаря которой вы сможете создавать собственный код пролога и эпилог.

Сведения о соглашениях о вызовах для процессоров x64 см. в разделе [соглашение о вызовах](../build/x64-calling-convention.md).

## <a name="topics-in-this-section"></a>Разделы этой статьи

- [Передача аргументов и соглашения об именовании](../cpp/argument-passing-and-naming-conventions.md) ( **`__cdecl`** ,, **`__stdcall`** **`__fastcall`** и др.)

- [Пример вызова: прототип функции и вызов](../cpp/calling-example-function-prototype-and-call.md)

- [Использование вызова функции с атрибутом naked для написания собственного кода пролога и эпилога](../cpp/naked-function-calls.md)

- [Соглашения о сопроцессоре и вызовах с плавающей точкой](../cpp/floating-point-coprocessor-and-calling-conventions.md)

- [Устаревшие соглашения о вызовах](../cpp/obsolete-calling-conventions.md)

## <a name="see-also"></a>См. также раздел

[Модификаторы, специфичные для Майкрософт](../cpp/microsoft-specific-modifiers.md)
