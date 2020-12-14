---
description: 'Дополнительные сведения: как добавить собственную библиотеку DLL в глобальный кэш сборок'
title: Практическое руководство. Добавление машинной библиотеки DLL в глобальный кэш сборок
ms.custom: get-started-article
ms.date: 11/04/2016
helpviewer_keywords:
- DLLs [C++], native
- GAC (global assembly cache), loading native DLLs
- native DLLs [C++]
ms.assetid: 25e8d78a-b197-4269-b4e9-237a544ab3c8
ms.openlocfilehash: 267bc2f08fdd40da03b71222c48786ab7cc150fd
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335412"
---
# <a name="how-to-add-native-dll-to-global-assembly-cache"></a>Практическое руководство. Добавление машинной библиотеки DLL в глобальный кэш сборок

В глобальный кэш сборок можно разместить собственную библиотеку DLL (не COM).

## <a name="example"></a>Пример

**/ASSEMBLYLINKRESOURCE** позволяет внедрить собственную библиотеку DLL в сборку.

Дополнительные сведения см. [в разделе/ASSEMBLYLINKRESOURCE (ссылка на ресурс .NET Framework)](../build/reference/assemblylinkresource-link-to-dotnet-framework-resource.md).

```
/ASSEMBLYLINKRESOURCE:MyComponent.dll
```

## <a name="see-also"></a>См. также раздел

[Использование взаимодействия C++ (неявный PInvoke)](../dotnet/using-cpp-interop-implicit-pinvoke.md)
