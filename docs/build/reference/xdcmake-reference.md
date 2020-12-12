---
description: Дополнительные сведения см. в справочнике по программе XDCMake.
title: Справочник по XDCMake
ms.date: 11/04/2016
f1_keywords:
- xdcmake
helpviewer_keywords:
- xdcmake program
ms.assetid: 14e65747-d000-4343-854b-8393bf01cbac
ms.openlocfilehash: c9e597828ca37b67a21a5b2f442fffcac001b541
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97260999"
---
# <a name="xdcmake-reference"></a>Справочник по XDCMake

xdcmake.exe — это программа, которая компилирует XDC-файлы в XML-файл. XDC-файл создается компилятором КОМПИЛЯТОРОМ MSVC для каждого файла исходного кода, когда исходный код компилируется с помощью [/doc](doc-process-documentation-comments-c-cpp.md) и когда файл исходного кода содержит комментарии к документации, помеченные тегами XML.

### <a name="to-use-xdcmakeexe-in-the-visual-studio-development-environment"></a>Использование xdcmake.exe в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Откройте папку **Свойства конфигурации**.

1. Выберите страницу свойств **Комментарии XML-документа**.

> [!NOTE]
> Параметры xdcmake.exe в командной строке отличаются от параметров, доступных при использовании xdcmake.exe из среды разработки (страницы свойств). Сведения об использовании xdcmake.exe в среде разработки см. в разделе [Страницы свойств средства создания XML-документов](xml-document-generator-tool-property-pages.md).

## <a name="syntax"></a>Синтаксис

xdcmake `input_filename options`

## <a name="parameters"></a>Параметры

*input_filename*<br/>
Имя для XDC-файлов, используемых в качестве входных для xdcmake.exe. Укажите один или несколько XDC-файлов или значение *.xdc, чтобы использовать все XDC-файлы в текущем каталоге.

*options*<br/>
От нуля до нескольких следующих параметров:

|Параметр|Описание|
|------------|-----------------|
|/?, /help|Отображает справку для xdcmake.exe.|
|/Assembly:*имя файла*|Позволяет указать значение \<assembly> тега в XML-файле.  По умолчанию значение \<assembly> тега соответствует имени файла XML-файла.|
|/nologo|Позволяет запретить вывод сообщения об авторских правах.|
|/out:*имя_файла*|Позволяет указать имя XML-файла.  По умолчанию именем XML-файла является имя первого XDC-файла, обработанного xdcmake.exe.|

## <a name="remarks"></a>Комментарии

Visual Studio вызовет xdcmake.exe автоматически при сборке проекта. Кроме того, xdcmake.exe можно вызвать из командной строки.

Дополнительные сведения о добавлении комментариев документации в файлы исходного кода см. в разделе [Рекомендуемые теги для комментариев документации](recommended-tags-for-documentation-comments-visual-cpp.md).

## <a name="see-also"></a>См. также раздел

[Документация XML](xml-documentation-visual-cpp.md)
