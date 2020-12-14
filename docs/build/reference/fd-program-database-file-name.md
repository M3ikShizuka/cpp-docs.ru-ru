---
description: Дополнительные сведения о параметре/FD (имя файла базы данных программы)
title: /Fd (имя файла базы данных программы)
ms.date: 11/04/2016
f1_keywords:
- /FD
- VC.Project.VCCLWCECompilerTool.ProgramDataBaseFileName
- VC.Project.VCCLCompilerTool.ProgramDataBaseFileName
helpviewer_keywords:
- /FD compiler option [C++]
- program database file name [C++]
- -FD compiler option [C++]
- PDB files, creating
- program database compiler option [C++]
- .pdb files, creating
- FD compiler option [C++]
ms.assetid: 3977a9ed-f0ac-45df-bf06-01cedd2ba85a
ms.openlocfilehash: 3990cdd6c560dfdeaef7078a29e965831c2a9504
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97200667"
---
# <a name="fd-program-database-file-name"></a>/Fd (имя файла базы данных программы)

Указывает имя файла для файла базы данных программы (PDB), созданного [/Z7,/Zi,/Zi (формат отладочной информации)](z7-zi-zi-debug-information-format.md).

## <a name="syntax"></a>Синтаксис

```
/Fdpathname
```

## <a name="remarks"></a>Remarks

Без **/FD** имя PDB-файла по умолчанию имеет значение VC *x* 0. pdb, где *x* — основной номер версии Visual C++ используется.

Если указать путь, который не включает имя файла (путь заканчивается обратной косой чертой), компилятор создает PDB-файл с именем VC *x* 0. pdb в указанном каталоге.

Если указать имя файла, не включающее расширение, компилятор использует расширение PDB в качестве расширения.

Этот параметр также присваивает имя файлу состояния (IDB), используемому для минимальной перестройки и добавочной компиляции.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **C/C++** .

1. Откройте страницу свойств **Выходные файлы** .

1. Измените значение свойства **имя файла базы данных программы** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.ProgramDataBaseFileName%2A>.

## <a name="example"></a>Пример

Эта командная строка создает PDB-файл с именем PROG. pdb и IDB-файлом с именем PROG. IDB:

```
CL /DDEBUG /Zi /FdPROG.PDB PROG.CPP
```

## <a name="see-also"></a>См. также раздел

[Параметры OUTPUT-File (/F)](output-file-f-options.md)<br/>
[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)<br/>
[Указание пути](specifying-the-pathname.md)
