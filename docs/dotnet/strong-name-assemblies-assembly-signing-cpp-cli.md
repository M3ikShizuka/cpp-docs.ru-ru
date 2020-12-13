---
description: 'Дополнительные сведения: сборки со строгими именами (подписывание сборок) (C++/CLI)'
title: Сборки со строгими именами (подписывание сборок) (C++/CLI)
ms.date: 11/04/2016
helpviewer_keywords:
- assemblies [C++]
- signing assemblies
- .NET Framework [C++], assembly signing
- assemblies [C++], signing
- linker [C++], assembly signing
- strong-named assemblies [C++]
ms.assetid: c337cd3f-e5dd-4c6f-a1ad-437e85dba1cc
ms.openlocfilehash: 9fc08df759fa384ed13dbe3d8c3eb2d843183517
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335310"
---
# <a name="strong-name-assemblies-assembly-signing-ccli"></a>Сборки со строгими именами (подписывание сборок) (C++/CLI)

В этом разделе обсуждается, как можно подписать сборку, часто называемую присвоением сборке строгого имени.

## <a name="remarks"></a>Комментарии

При использовании Visual C++ используйте параметры компоновщика для подписывания сборки, чтобы избежать проблем, связанных с атрибутами CLR для подписывания сборки:

- <xref:System.Reflection.AssemblyDelaySignAttribute>

- <xref:System.Reflection.AssemblyKeyFileAttribute>

- <xref:System.Reflection.AssemblyKeyNameAttribute>

Причины отсутствия использования атрибутов включают в себя тот факт, что имя ключа отображается в метаданных сборки, что может представлять угрозу безопасности, если имя файла содержит конфиденциальную информацию. Кроме того, процесс сборки, используемый средой разработки Visual C++, сделает ключ, с которым подписана сборками, недействительным, если использовать атрибуты CLR для присвоения сборке строгого имени, а затем запустить для сборки средство завершающей обработки, такое как mt.exe.

Если вы выполняете сборку в командной строке, используйте параметры компоновщика для подписывания сборки, а затем запустите средство последующей обработки (например, mt.exe), необходимо повторно подписать сборку с sn.exe. Кроме того, можно создать и отложить подпись сборки и после запуска средств последующей обработки завершить подписывание.

Если атрибуты подписывания используются при построении в среде разработки, сборку можно успешно подписать, явно вызвав sn.exe ([Sn.exe (средство строгих имен)](/dotnet/framework/tools/sn-exe-strong-name-tool)) в событии после сборки. Дополнительные сведения см. в разделе [Задание событий сборки](../build/specifying-build-events.md). Время сборки может быть меньше, если используются атрибуты и событие после сборки по сравнению с использованием параметров компоновщика.

Следующие параметры компоновщика поддерживают подписывание сборок:

- [/DELAYSIGN (частичное подписание сборки)](../build/reference/delaysign-partially-sign-an-assembly.md)

- [/KEYFILE (указание ключа или пары ключей для подписи сборки)](../build/reference/keyfile-specify-key-or-key-pair-to-sign-an-assembly.md)

- [/KEYCONTAINER (указание контейнера ключей для подписи сборки)](../build/reference/keycontainer-specify-a-key-container-to-sign-an-assembly.md)

Дополнительные сведения о строгих сборках см. в разделе [Создание и использование Strong-Named сборок](/dotnet/framework/app-domains/create-and-use-strong-named-assemblies).

## <a name="see-also"></a>См. также раздел

[Программирование .NET с использованием C++/CLI (Visual C++)](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)
