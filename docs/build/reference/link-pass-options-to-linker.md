---
description: Подробнее о:/Link (передача параметров компоновщику)
title: /link (Передача параметров компоновщику)
ms.date: 03/25/2019
f1_keywords:
- /link
helpviewer_keywords:
- /link compiler option [C++]
- pass options to linker
- link compiler option [C++]
- linker [C++], passing options to
- -link compiler option [C++]
- cl.exe compiler [C++], passing options to linker
ms.assetid: 16902a94-c094-4328-841f-3ac94ca04848
ms.openlocfilehash: 3617a005e6adbc41a589606aa145712fa2df442d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97199497"
---
# <a name="link-pass-options-to-linker"></a>/link (Передача параметров компоновщику)

Передает компоновщику один или несколько параметров компоновщика.

## <a name="syntax"></a>Синтаксис

> **/Link** *-Параметры компоновщика*

## <a name="arguments"></a>Аргументы

*параметры компоновщика*<br/>
Параметр компоновщика или параметры, передаваемые компоновщику.

## <a name="remarks"></a>Комментарии

Параметр **/Link** и его параметры компоновщика должны присутствовать после имен файлов и параметров CL. Требуется пробел между **/Link** и параметрами компоновщика. Дополнительные сведения см. в разделе [Справочник по компоновщику компилятором MSVC](linking.md).

## <a name="example"></a>Пример

Этот пример командной строки компилирует *Hello. cpp* и связывает его с существующим объектом Object в файле *. obj*. Затем он передает компоновщику дополнительную команду **/Version** :

`cl /W4 /EHsc hello.cpp there.obj /link /VERSION:3.14`

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

Интегрированная среда разработки обычно отправляет отдельные команды для компиляции и связывания кода. Параметры компоновщика можно задать на страницах свойств проекта.

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку   >  **компоновщика** свойства конфигурации.

1. Измените одно или несколько свойств. Выберите **ОК** для сохранения внесенных изменений.

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- Этот параметр компилятора нельзя изменить программным способом.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
