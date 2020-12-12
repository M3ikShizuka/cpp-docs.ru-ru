---
description: Дополнительные сведения о странице свойств "управляемые ресурсы"
title: страница свойств управляемых ресурсов
ms.date: 08/28/2019
f1_keywords:
- VC.Project.VCManagedResourceCompilerTool.ResourceFileName
- VC.Project.VCManagedResourceCompilerTool.OutputFileName
- VC.Project.VCManagedResourceCompilerTool.DefaultLocalizedResources
helpviewer_keywords:
- Managed Resources property page
ms.assetid: 80b80384-ee55-494d-9f0e-907bb98cfc19
ms.openlocfilehash: 42816e2b4625bc5ab4620f4caafb627f55bd9cd5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97190722"
---
# <a name="managed-resources-property-page"></a>страница свойств управляемых ресурсов

На странице свойств **управляемые ресурсы** отображаются следующие свойства [resgen.exe](/dotnet/framework/tools/resgen-exe-resource-file-generator) компилятора управляемых ресурсов при использовании ресурсов .NET в программах C++/CLI:

- **Логическое имя ресурса**

   Указывает *логическое имя* для созданного промежуточного файла RESOURCES. Логическое имя используется для загрузки ресурса. Если логическое имя не указано, вместо него используется имя файла ресурсов (RESX).

- **Имя выходного файла**

   Указывает имя окончательного выходного файла, в который направляется этот файл ресурсов (RESX).

- **Локализованные ресурсы по умолчанию**

   Указывает, направляется ли данный файл RESX в ресурсы по умолчанию либо во вспомогательную библиотеку DLL.

Сведения о том, как получить доступ к странице свойств **управляемых ресурсов** , см. [в разделе Установка компилятора C++ и свойств сборки в Visual Studio](../working-with-project-properties.md).

## <a name="see-also"></a>См. также раздел

[Использование компилятора ресурсов (командная строка RC)](/windows/win32/menurc/using-rc-the-rc-command-line-)<br>
[Справочник по страницам свойств проекта C++](property-pages-visual-cpp.md)<br>
[/ASSEMBLYRESOURCE (внедрение управляемого ресурса)](assemblyresource-embed-a-managed-resource.md)
