---
description: Дополнительные сведения о:/V (номер версии)
title: /V (номер версии)
ms.date: 11/04/2016
f1_keywords:
- /v
helpviewer_keywords:
- embedding version strings
- /V compiler option [C++]
- version numbers, specifying for .obj
- V compiler option [C++]
- -V compiler option [C++]
ms.assetid: 3e93fb7a-5dfd-49a6-bd49-3dca8052e0f3
ms.openlocfilehash: 5025642d4ae30315d24754a7ee46268050cfb22a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97187056"
---
# <a name="v-version-number"></a>/V (номер версии)

Не рекомендуется. Внедряет текстовую строку в OBJ-файл.

## <a name="syntax"></a>Синтаксис

```
/Vstring
```

## <a name="arguments"></a>Аргументы

*строка*<br/>
Строка, указывающая номер версии или уведомление об авторском праве, которые должны быть внедрены в OBJ-файл.

## <a name="remarks"></a>Комментарии

Стрингкан метка OBJ-файла с номером версии или уведомлением об авторских правах. Любые пробелы или символы табуляции должны быть заключены в двойные кавычки ("), если они являются частью строки. Обратная косая черта ( \\ ) должна предшествовать любым двойным кавычкам, если они являются частью строки. Пробел между **/v** и `string` является необязательным.

Можно также использовать [комментарий (C/C++)](../../preprocessor/comment-c-cpp.md) с аргументом компилятора-Type комментария, чтобы разместить имя и номер версии компилятора в файле obj.

Параметр **/v** является устаревшим, начиная с Visual Studio 2005; Параметр **/v** в основном использовался для поддержки создания драйверов виртуальных устройств (VxD), а сборка VxD больше не поддерживается набором инструментов Visual C++. Список устаревших параметров компилятора см. в разделе **устаревшие и удаленные параметры** компилятора в [параметрах компилятора, перечисленных по категориям](compiler-options-listed-by-category.md).

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Выберите страницу свойств **Командная строка** .

1. Введите параметр компилятора в поле **Дополнительные параметры** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
