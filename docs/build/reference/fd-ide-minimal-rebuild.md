---
description: Подробнее о:/FD (минимальное перестроение IDE)
title: Параметр /FD (минимальное перестроение интерфейса IDE)
ms.date: 04/08/2019
helpviewer_keywords:
- /FD compiler option [C++]
- -FD compiler option [C++]
- FD compiler option [C++]
ms.assetid: 7ef21b8c-a448-4bb4-9585-a2a870028e17
ms.openlocfilehash: d9b2a91c14b80890c703b8f4dd5b2de3aefb012b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97192295"
---
# <a name="fd-ide-minimal-rebuild"></a>Параметр /FD (минимальное перестроение интерфейса IDE)

Параметр **/FD** предоставляется только пользователям на странице свойств [Командная строка](command-line-property-pages.md) диалогового окна **страницы свойств** проекта C++. Он доступен только в том случае, если не выбран параметр [/GM (включение минимального перестроения) (](gm-enable-minimal-rebuild.md) нерекомендуемый и отключенный по умолчанию). Параметр **/FD** не оказывает никакого воздействия, кроме среды разработки. Параметр **/FD** не предоставляется в выходных данных `cl /?` .

Если не включить нерекомендуемый параметр **/GM** в среде разработки, то используется **/FD** . **/FD** гарантирует, что IDB файл имеет достаточно сведений о зависимостях. Параметр **/FD** используется только средой разработки и не должен использоваться из командной строки или скрипта сборки.

## <a name="see-also"></a>См. также раздел

[Параметры OUTPUT-File (/F)](output-file-f-options.md)<br/>
[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
