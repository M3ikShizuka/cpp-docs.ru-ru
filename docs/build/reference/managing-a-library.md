---
description: Дополнительные сведения см. в статье Управление библиотекой.
title: Управление библиотекой
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLibrarianTool.OVERWRITEAllDefaultLibraries
- VC.Project.VCLibrarianTool.AdditionalDependencies
- VC.Project.VCLibrarianTool.RemoveObjects
- VC.Project.VCLibrarianTool.LibraryPaths
- VC.Project.VCLibrarianTool.OutputFile
- VC.Project.VCLibrarianTool.OVERWRITEDefaultLibraryNames
- VC.Project.VCLibrarianTool.AdditionalLibraryDirectories
- VC.Project.VCLibrarianTool.ListContentsFile
- VC.Project.VCLibrarianTool.ListContents
- VC.Project.VCLibrarianTool.SubSystemVersion
- VC.Project.VCLibrarianTool.OVERWRITEDefaultLibraryName
- VC.Project.VCLibrarianTool.SubSystem
helpviewer_keywords:
- /LIBPATH library manager option
- OUT library manager option
- CONVERT library manager option
- LIBPATH library manager option
- /LIST library manager option
- object files, building and modifying
- -LINK50COMPAT library manager option
- REMOVE library manager option
- SUBSYSTEM library manager option
- /LINK50COMPAT library manager option
- /OUT library manager option
- LIB [C++], managing COFF libraries
- -CONVERT library manager option
- LINK50COMPAT library manager option
- -OUT library manager option
- -REMOVE library manager option
- -LIST library manager option
- /SUBSYSTEM library manager option
- -SUBSYSTEM library manager option
- /REMOVE library manager option
- -LIBPATH library manager option
- object files
- LIST library manager option
- /CONVERT library manager option
ms.assetid: f56a8b85-fbdc-4c09-8d8e-00f0ffe1da53
ms.openlocfilehash: f862dfd460bb51cdf6e855c87b08b7426a5642d0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97199133"
---
# <a name="managing-a-library"></a>Управление библиотекой

Режимом по умолчанию для LIB является создание или изменение библиотеки объектов COFF. LIB работает в этом режиме, если не указать параметр/EXTRACT (для копирования объекта в файл) или/DEF (для построения библиотеки импорта).

Чтобы создать библиотеку из объектов и (или) библиотек, используйте следующий синтаксис:

```
LIB [options...] files...
```

Эта команда создает библиотеку из одного или нескольких входных *файлов*. *Файлы* могут представлять собой объектные файлы COFF, 32-разрядные файлы OMF или существующие библиотеки COFF. LIB создает одну библиотеку, которая содержит все объекты в указанных файлах. Если входной файл является 32-битным объектным файлом OMF, программа LIB преобразует его в COFF перед сборкой библиотеки. LIB не может принимать 32-разрядный объект OMF, который находится в библиотеке, созданной 16-разрядной версией LIB. Для извлечения объекта необходимо сначала использовать 16-разрядную версию LIB. Затем можно использовать извлеченный объектный файл в качестве входных данных для 32-разрядной библиотеки LIB.

По умолчанию LIB присваивает выходному файлу базовое имя первого объекта или файла библиотеки и Extension. lib. Выходной файл помещается в текущий каталог. Если файл с таким именем уже существует, то выходной файл заменит существующий файл. Чтобы сохранить существующую библиотеку, используйте параметр/OUT, чтобы указать имя выходного файла.

Для создания и изменения библиотеки применяются следующие параметры.

**/Libpath:** *dir*<br/>
Переопределяет путь к библиотеке среды. Дополнительные сведения см. в описании параметра LINK [/libpath](libpath-additional-libpath.md) .

**/LIST**<br/>
Отображает сведения о выходной библиотеке для стандартного вывода. Выходные данные можно перенаправить в файл. С помощью/LIST можно определить содержимое существующей библиотеки, не изменяя ее.

**/Name:** *имя файла*<br/>
При построении библиотеки импорта указывает имя библиотеки DLL, для которой строится библиотека импорта.

**/NODEFAULTLIB**<br/>
Удаляет одну или несколько библиотек по умолчанию из списка библиотек, поиск которых выполняется при разрешении внешних ссылок. Дополнительные сведения см. в разделе [/NODEFAULTLIB](nodefaultlib-ignore-libraries.md) .

**/Out:** *имя файла*<br/>
Переопределяет имя выходного файла по умолчанию. По умолчанию выходная библиотека создается в текущем каталоге, базовое имя первой библиотеки или объектного файла — в командной строке и в файле Extension. lib.

**/Remove:** *объект*<br/>
Исключает указанный *объект* из выходной библиотеки. LIB создает выходную библиотеку, объединяя все объекты (в объектных файлах или библиотеках), а затем удаляя все объекты, указанные с помощью/РЕМОВЕ.

**/SUBSYSTEM:**{**CONSOLE** &#124; **EFI_APPLICATION** &#124; **EFI_BOOT_SERVICE_DRIVER** &#124; **EFI_ROM** &#124; **EFI_RUNTIME_DRIVER** &#124; **native** &#124; **POSIX** &#124; **Windows** &#124; **WindowsCE**} [, # [. # #]]<br/>
Указывает операционной системе, как запустить программу, созданную путем связывания с выходной библиотекой. Дополнительные сведения см. в описании параметра LINK [/SUBSYSTEM](subsystem-specify-subsystem.md) .

Параметры LIB, указанные в командной строке, не учитывают регистр.

С помощью LIB можно выполнять следующие задачи управления библиотекой:

- Чтобы добавить объекты в библиотеку, укажите имя файла для существующей библиотеки и имена файлов для новых объектов.

- Чтобы объединить библиотеки, укажите имена файлов библиотеки. Вы можете добавлять объекты и объединять библиотеки с помощью одной команды LIB.

- Чтобы заменить член библиотеки новым объектом, укажите библиотеку, содержащую заменяемый объект-член, и имя файла для нового объекта (или библиотеки, содержащей его). Если объект с таким же именем существует в нескольких входных файлах, LIB помещает последний объект, указанный в команде LIB, в выходную библиотеку. При замене элемента библиотеки обязательно укажите новый объект или библиотеку после библиотеки, содержащей старый объект.

- Чтобы удалить элемент из библиотеки, используйте параметр/REMOVE. LIB обрабатывает все спецификации/REMOVE после объединения всех входных объектов, независимо от порядка командной строки.

> [!NOTE]
> Нельзя одновременно удалить элемент и извлечь его в файл на том же шаге. Сначала необходимо извлечь объект члена с помощью команды/EXTRACT, а затем снова запустить программу LIB с помощью/РЕМОВЕ. Это поведение отличается от 16-разрядной библиотеки (для библиотек OMF), предоставляемой другими продуктами Майкрософт.

## <a name="see-also"></a>См. также раздел

[Справочник по LIB](lib-reference.md)
