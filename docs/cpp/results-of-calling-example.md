---
description: 'Дополнительные сведения о: результаты вызова примера'
title: Пример результатов вызова
ms.date: 11/19/2018
helpviewer_keywords:
- examples [C++], results of calling
- results, thiscall call
- results, __fastcall keyword call
- results, __cdecl call
- results, __stdcall call
ms.assetid: aa70a7cb-ba1d-4aa6-bd0a-ba783da2e642
ms.openlocfilehash: 91da3182742414dc4850013463b74ae36aa782c0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97262923"
---
# <a name="results-of-calling-example"></a>Пример результатов вызова

**Блок, относящийся только к системам Microsoft**

## <a name="__cdecl"></a>__cdecl

Имя функции с декорированием в C — `_MyFunc` .

![Соглашение о вызовах CDECL](../cpp/media/vc37i01.gif "Соглашение о вызовах CDECL") <br/>
**`__cdecl`** Соглашение о вызовах

## <a name="__stdcall-and-thiscall"></a>__stdcall и thiscall

Декорированное имя C ( **`__stdcall`** ) имеет значение `_MyFunc@20` . Декорированное имя C++ зависит от конкретной реализации.

![ Соглашения о вызовах&#95;&#95;STDCALL и thiscall](../cpp/media/vc37i02.gif "Соглашения о вызовах &#95;&#95;STDCALL и thiscall") <br/>
Соглашения о вызовах __stdcall и thiscall

## <a name="__fastcall"></a>__fastcall

Декорированное имя C ( **`__fastcall`** ) имеет значение `@MyFunc@20` . Декорированное имя C++ зависит от конкретной реализации.

![Соглашение о вызовах для &#95;&#95;fastcall](../cpp/media/vc37i03.gif "Соглашение о вызовах для &#95;&#95;fastcall") <br/>
Соглашение о вызовах __fastcall

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Пример вызова: прототип функции и вызов](../cpp/calling-example-function-prototype-and-call.md)
