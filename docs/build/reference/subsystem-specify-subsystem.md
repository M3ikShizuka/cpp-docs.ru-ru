---
description: Подробнее о:/SUBSYSTEM (указание подсистемы)
title: /SUBSYSTEM (укажите подсистему)
ms.date: 11/04/2016
f1_keywords:
- /subsystem
- VC.Project.VCLinkerTool.SubSystem
- VC.Project.VCLinkerTool.SubSystemVersion
helpviewer_keywords:
- /SUBSYSTEM linker option
- SUBSYSTEM linker option
- -SUBSYSTEM linker option
- subsystem specifications
ms.assetid: d7b133cf-cf22-4da8-ab46-6552702c0b9b
ms.openlocfilehash: 18a8ad549cc4aa1e143e43619d549c9eb7ae7324
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97236247"
---
# <a name="subsystem-specify-subsystem"></a>/SUBSYSTEM (укажите подсистему)

```
/SUBSYSTEM:{BOOT_APPLICATION|CONSOLE|EFI_APPLICATION|
            EFI_BOOT_SERVICE_DRIVER|EFI_ROM|EFI_RUNTIME_DRIVER|NATIVE|
            POSIX|WINDOWS)
            [,major[.minor]]
```

## <a name="arguments"></a>Аргументы

**BOOT_APPLICATION**<br/>
Приложение, которое выполняется в среде загрузки Windows. Дополнительные сведения о приложениях загрузки см. в разделе [About BCD](/previous-versions/windows/desktop/bcd/about-bcd).

**КОНСОЛ**<br/>
Приложение в символьном режиме Win32. Операционная система предоставляет консоль для консольных приложений. Если `main` или `wmain` определен для машинного кода, `int main(array<String ^> ^)` определяется для управляемого кода или полностью строится с помощью `/clr:safe` , по умолчанию используется консоль.

**EFI_APPLICATION**<br/>
**EFI_BOOT_SERVICE_DRIVER**<br/>
**EFI_ROM**<br/>
**EFI_RUNTIME_DRIVER**<br/>
Расширяемые подсистемы интерфейса встроенного по. Дополнительные сведения см. в спецификации EFI. Примеры см. на веб-сайте Intel. Минимальная версия и версия по умолчанию — 1,0.

**СОБСТВЕННОЙ**<br/>
Драйверы режима ядра для Windows NT. Этот параметр обычно зарезервирован для системных компонентов Windows. Если параметр [/Driver: WDM](driver-windows-nt-kernel-mode-driver.md) указан, по умолчанию используется Native.

**POSIX**<br/>
Приложение, работающее с подсистемой POSIX в Windows NT.

**WINDOWS**<br/>
Приложению не требуется консоль, возможно, из-за того, что она создает собственные окна для взаимодействия с пользователем. Если `WinMain` или определен `wWinMain` для машинного кода или `WinMain(HISTANCE *, HINSTANCE *, char *, int)` `wWinMain(HINSTANCE *, HINSTANCE *, wchar_t *, int)` определен для управляемого кода, Windows является значением по умолчанию.

*основной* и *дополнительный*<br/>
Используемых Укажите минимальную требуемую версию подсистемы. Аргументы являются десятичными числами в диапазоне от 0 до 65 535. Дополнительные сведения см. в примечаниях. Верхних границ для номеров версий нет.

## <a name="remarks"></a>Комментарии

Параметр **/SUBSYSTEM** задает среду для исполняемого файла.

Выбор подсистемы влияет на символ точки входа (или функцию точки входа), который будет выбран компоновщиком.

Ниже приведены необязательные и *основные* и дополнительные *номера версий по* умолчанию для подсистем.

|Subsystem|Минимальные|Значение по умолчанию|
|---------------|-------------|-------------|
|BOOT_APPLICATION|1.0|1.0|
|CONSOLE|5,01 (x86) 5,02 (x64) 6,02 (ARM)|6,00 (x86, x64) 6,02 (ARM)|
|WINDOWS|5,01 (x86) 5,02 (x64) 6,02 (ARM)|6,00 (x86, x64) 6,02 (ARM)|
|NATIVE (с ДРАЙВЕРом: WDM)|1,00 (x86) 1,10 (x64, ARM)|1,00 (x86) 1,10 (x64, ARM)|
|NATIVE (без/DRIVER: WDM)|4,00 (x86) 5,02 (x64) 6,02 (ARM)|4,00 (x86) 5,02 (x64) 6,02 (ARM)|
|POSIX|1.0|19.90|
|EFI_APPLICATION, EFI_BOOT_SERVICE_DRIVER, EFI_ROM, EFI_RUNTIME_DRIVER|1.0|1.0|

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку Компоновщик.

1. Выберите страницу свойств **системы** .

1. Измените `SubSystem` свойство.

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.SubSystem%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
