---
description: 'Дополнительные сведения: предотвращение исключений при завершении работы среды CLR при использовании COM-объектов, созданных с помощью/CLR'
title: Исключение исключений, создаваемых COM-объектами, созданными с помощью среды CLR
ms.date: 11/04/2016
helpviewer_keywords:
- interop [C++], CLR shutdown exceptions
- /clr compiler option [C++], CLR shutdown exceptions
- mixed assemblies [C++], CLR shutdown exceptions
- /clr compiler option [C++], COM objects
- interoperability [C++], CLR shutdown exceptions
- CLR shutdown exceptions [C++]
ms.assetid: 41249d83-4b51-4e46-866f-27f475f2498c
ms.openlocfilehash: 899f7905aafcf1bff92e37ee70253e74759b3f57
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97282618"
---
# <a name="avoiding-exceptions-on-clr-shutdown-when-consuming-com-objects-built-with-clr"></a>Способы избегания исключений во время завершения работы среды CLR при использовании COM-объектов, построенных с помощью /clr

Когда среда CLR переходит в режим завершения работы, собственные функции имеют ограниченный доступ к службам CLR. При попытке вызвать Release для COM-объекта, скомпилированного с **параметром/CLR**, среда CLR переходит в машинный код, а затем обратно в управляемый код для обслуживания вызова IUnknown:: Release (который определен в управляемом коде). Среда CLR предотвращает обратный вызов управляемого кода, так как он находится в режиме завершения работы.

Чтобы устранить эту проблему, убедитесь, что деструкторы, вызываемые из методов выпуска, содержат только машинный код.

## <a name="see-also"></a>См. также раздел

[Смешанные (собственные и управляемые) сборки](../dotnet/mixed-native-and-managed-assemblies.md)
