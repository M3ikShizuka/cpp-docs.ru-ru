---
description: Дополнительные сведения о:/PGD (указание базы данных для оптимизации Profile-Guided)
title: /PGD (указание базы данных для профильной оптимизации)
ms.date: 03/14/2018
f1_keywords:
- VC.Project.VCLinkerTool.ProfileGuidedDatabase
helpviewer_keywords:
- -PGD linker option
- /PGD linker option
ms.assetid: 9f312498-493b-461f-886f-92652257e443
ms.openlocfilehash: 7030ddaef33c6ee794c470df2c42c72d78555369
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97225990"
---
# <a name="pgd-specify-database-for-profile-guided-optimizations"></a>/PGD (указание базы данных для профильной оптимизации)

**Параметр/PGD является устаревшим.** Начиная с Visual Studio 2015 вместо них предпочтительнее использовать параметры компоновщика [/GENPROFILE или/FASTGENPROFILE](genprofile-fastgenprofile-generate-profiling-instrumented-build.md) . Этот параметр используется для указания имени PGD-файла, используемого процессом профильной оптимизации.

## <a name="syntax"></a>Синтаксис

> **/PGD:**_имя файла_

## <a name="argument"></a>Аргумент

*filename*<br/>
Указывает имя PGD-файла, который используется для хранения сведений об выполняющейся программе.

## <a name="remarks"></a>Комментарии

При использовании устаревшего параметра [/LTCG: PGINSTRUMENT](ltcg-link-time-code-generation.md) используйте параметр **/PGD** , чтобы указать имя или расположение PGD-файла по умолчанию. Если параметр **/PGD** не указан, базовое имя файла PGD совпадает с базовым именем выходного файла (exe или DLL) и создается в том же каталоге, из которого была вызвана ссылка.

При использовании устаревшего параметра **/LTCG: PGOPTIMIZE** используйте параметр **/PGD** , чтобы указать имя PGD файла, который будет использоваться для создания оптимизированного образа. Аргумент *filename* должен совпадать с *именем файла* , указанным для **/LTCG: PGINSTRUMENT**.

Дополнительные сведения см. в статье [Профильные оптимизации](../profile-guided-optimizations.md).

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите   >    >  страницу свойств **Оптимизация** компоновщика свойств конфигурации.

1. Изменение свойства **базы данных, управляемой профилем** . Выберите **ОК** для сохранения внесенных изменений.

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

1. См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ProfileGuidedDatabase%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)<br/>
