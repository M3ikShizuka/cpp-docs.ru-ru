---
description: 'Дополнительные сведения: предупреждение компилятора (уровень 3) C4192'
title: Предупреждение компилятора (уровень 3) C4192
ms.date: 11/04/2016
f1_keywords:
- C4192
helpviewer_keywords:
- C4192
ms.assetid: ea5f91fa-8c96-4f3f-ac42-0c8a86d4e5df
ms.openlocfilehash: 8cfebf1845c578723bab5622e18699c0282d4c4b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97344228"
---
# <a name="compiler-warning-level-3-c4192"></a>Предупреждение компилятора (уровень 3) C4192

автоматически исключить "Name" при импорте библиотеки типов "Library"

`#import`Библиотека содержит элемент, *имя*, которое также определено в заголовках системы Win32. Из-за ограничений библиотек типов такие имена, как **IUnknown** или GUID, часто определяются в библиотеке типов, что приводит к дублированию определения из системных заголовков. `#import` обнаружит эти элементы и отказывается их внедрять в файлы заголовков TLH и тли.

Чтобы переопределить это поведение, используйте `#import` атрибуты [no_auto_exclude](../../preprocessor/no-auto-exclude.md) и [include ()](../../preprocessor/include-parens.md).
