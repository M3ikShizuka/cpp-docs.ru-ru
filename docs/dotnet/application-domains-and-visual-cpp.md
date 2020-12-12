---
description: 'Дополнительные сведения: домены приложений и Visual C++'
title: Домены приложений и Visual C++
ms.date: 11/04/2016
helpviewer_keywords:
- interop [C++], application domains
- application domains [C++], C++
- /clr compiler option [C++], application domains
- interoperability [C++], application domains
- mixed assemblies [C++], application domains
ms.assetid: 75a08efc-9b02-40ba-99b7-dcbd71010bbf
ms.openlocfilehash: 55f02aec7b3b2d23f10ae9142dba7c61ff60683f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97282826"
---
# <a name="application-domains-and-visual-c"></a>Домены приложений и Visual C++

Если у вас есть `__clrcall` Виртуальная функция, то таблица vtable будет использоваться для каждого домена приложений (AppDomain). При создании объекта в одном AppDomain можно вызвать только виртуальную функцию из этого AppDomain. В смешанном режиме (**/CLR**) у вас будут виртуальные таблицы vtable для каждого процесса, если у вашего типа нет `__clrcall` виртуальных функций. Параметры компилятора **/clr: pure** и **/clr: Сейф** являются устаревшими в Visual Studio 2015 и не поддерживаются в Visual Studio 2017.

Дополнительные сведения см. в разделе:

- [класс](../cpp/appdomain.md)

- [__clrcall](../cpp/clrcall.md)

- [процесс](../cpp/process.md)

## <a name="see-also"></a>См. также раздел

- [Смешанные (собственные и управляемые) сборки](../dotnet/mixed-native-and-managed-assemblies.md)
