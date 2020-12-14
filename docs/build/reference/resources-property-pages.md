---
description: См. Дополнительные сведения о странице свойств ресурсов
title: Ресурсы
ms.date: 08/28/2019
ms.topic: article
ms.assetid: dade2f6b-c51f-4c33-9023-41956ae4b5f6
f1_keywords:
- VC.Project.VCResourceCompilerTool.PreprocessorDefinitions
- VC.Project.VCResourceCompilerTool.UndefineProcessorDefinitions
- VC.Project.VCResourceCompilerTool.Culture
- VC.Project.VCResourceCompilerTool.AdditionalIncludeDirectories
- VC.Project.VCResourceCompilerTool.IgnoreStandardIncludePath
- VC.Project.VCResourceCompilerTool.ShowProgress
- VC.Project.VCResourceCompilerTool.SuppressStartupBanner
- VC.Project.VCResourceCompilerTool.ResourceOutputFileName
- VC.Project.VCResourceCompilerTool.NullTerminateStrings
- vc.project.AdditionalOptionsPage
ms.openlocfilehash: d074cbb6035bd138ca322197e50e9a3f892b325b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97225106"
---
# <a name="resources-property-page"></a>Страница свойств ресурсов

Для настольных программ Windows сборка вызывает [компилятор ресурсов (rc.exe)](/windows/win32/menurc/resource-compiler) , чтобы добавить в двоичный файл изображения, таблицы строк и *RES* -файлы. Свойства, представленные на этой странице свойств, передаются компилятору ресурсов, а не компилятору C++ или компоновщику. Дополнительные сведения о свойствах, перечисленных здесь, и о том, как они сопоставляются с параметрами командной строки RC, см. в разделе Использование версии- [кандидата (Командная строка RC)](/windows/win32/menurc/using-rc-the-rc-command-line-). Сведения о том, как получить доступ к страницам свойств **ресурсов** , см. [в разделе Установка компилятора C++ и свойств сборки в Visual Studio](../working-with-project-properties.md). Для программного доступа к этим свойствам см. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCResourceCompilerTool>.

Свойства ресурсов .NET в приложениях C++/CLI отображаются на [странице свойств управляемые ресурсы](managed-resources-property-page.md).

## <a name="preprocessor-definitions"></a>Определения препроцессора

Указывает одно или несколько определений для компилятора ресурсов. (/d [макрос])

## <a name="undefine-preprocessor-definitions"></a>Отменить определения препроцессора

Отменить определение символа. /u

## <a name="culture"></a>culture

Список языка и региональных параметров (например, английского (США) или итальянского), используемых в ресурсах. (/l [число])

## <a name="additional-include-directories"></a>Дополнительные каталоги включаемых файлов

Указывает один или несколько каталогов для добавления к пути включения; Используйте точку с запятой в качестве разделителя, если он больше одного. (/I [путь])

## <a name="ignore-standard-include-paths"></a>Игнорировать стандартные пути включаемых файлов

Не дает компилятору ресурсов искать включаемые файлы в каталогах, указанных в переменных среды INCLUDE. /X

## <a name="show-progress"></a>Отображать ход выполнения

Отправка сообщений о ходе выполнения в окно вывода. /v

## <a name="suppress-startup-banner"></a>Отключить загрузочный баннер

Отключение отображения загрузочного баннера и информационного сообщения (/NOLOGO)

## <a name="resource-file-name"></a>Имя файла ресурсов

Указывает имя файла ресурсов (/FO [файл])

## <a name="null-terminate-strings"></a>Строки завершения со значением NULL

Добавьте значения NULL ко всем строкам в таблицах строк. параметра

## <a name="see-also"></a>См. также

[Справочник по страницам свойств проекта C++](property-pages-visual-cpp.md)
