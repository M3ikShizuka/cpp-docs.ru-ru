---
description: 'Дополнительные сведения:/FU (имя принудительно #using файл)'
title: '/FU (именование файла с принудительно используемым атрибутом #using)'
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCCLCompilerTool.ForcedUsingFiles
- /FU
- VC.Project.VCNMakeTool.ForcedUsingAssemblies
helpviewer_keywords:
- -FU compiler option [C++]
- FU compiler option [C++]
- /FU compiler option [C++]
ms.assetid: 698f8603-457f-435a-baff-5ac9243d6ca1
ms.openlocfilehash: 458369e7ff1322d2d2fa2fb37e8915c5a39c8446
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97200381"
---
# <a name="fu-name-forced-using-file"></a>/FU (именование файла с принудительно используемым атрибутом #using)

Параметр компилятора, который можно использовать в качестве альтернативы передаче имени файла в [директиву #using](../../preprocessor/hash-using-directive-cpp.md) в исходном коде.

## <a name="syntax"></a>Синтаксис

> **/FU** *файл*

## <a name="arguments"></a>Аргументы

*файл*<br/>
Указывает файл метаданных для ссылки в этой компиляции.

## <a name="remarks"></a>Комментарии

Параметр/FU принимает только одно имя файла. Чтобы указать несколько файлов, используйте/FU с каждым из них.

Если вы используете C++/CLI и ссылаетсяе на метаданные для использования функции [дружественных сборок](../../dotnet/friend-assemblies-cpp.md) , то нельзя использовать **/Fu**. Необходимо ссылаться на метаданные в коде с помощью `#using` — вместе с `[as friend]` атрибутом. Дружественные сборки не поддерживаются в Visual C++ расширениях компонентов C++/CX.

Сведения о создании сборки или модуля для среды CLR см. в разделе [/CLR (компиляция среды CLR)](clr-common-language-runtime-compilation.md). Сведения о построении в C++/CX см. в разделе [Создание приложений и библиотек](../../cppcx/building-apps-and-libraries-c-cx.md).

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите страницу свойств свойства **конфигурации**  >  **C/C++**  >  **Дополнительно** .

1. Измените свойство **Force #using** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.ForcedUsingFiles%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры OUTPUT-File (/F)](output-file-f-options.md)<br/>
[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
