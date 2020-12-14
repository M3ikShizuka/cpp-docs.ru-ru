---
description: Дополнительные сведения о:/F (установка размера стека)
title: /F (Задание размера стека)
ms.date: 11/04/2016
f1_keywords:
- /f
helpviewer_keywords:
- set stack size compiler option
- F compiler option [C++]
- -F compiler option [C++]
- /F compiler option [C++]
- stack, setting size
ms.assetid: 17320b6f-8305-445b-9ec2-75833f4b29e0
ms.openlocfilehash: 5bf8b0855c65fc39caf8935b06a877c62a4e0df0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97200784"
---
# <a name="f-set-stack-size"></a>/F (Задание размера стека)

Задает размер стека программы в байтах.

## <a name="syntax"></a>Синтаксис

> **/F** *число*

## <a name="arguments"></a>Аргументы

*number*<br/>
Размер стека в байтах.

## <a name="remarks"></a>Комментарии

Без этого параметра размер стека по умолчанию равен 1 МБ. Аргумент *Number* может быть в десятичном формате или в нотации языка C. Аргумент может находиться в диапазоне от 1 до максимального размера стека, принимаемого компоновщиком. Компоновщик Округляет указанное значение до ближайших 4 байт. Пробел между **/f** и *Number* является необязательным.

Если программа получает сообщения переполнения стека, может потребоваться увеличить размер стека.

Размер стека также можно задать следующим образом:

- Использование параметра компоновщика **/Stack** . Дополнительные сведения см. в разделе [/Stack](stack.md).

- Использование программы EDITBIN в файле exe. Дополнительные сведения см. в разделе [Справочник по EDITBIN](editbin-reference.md).

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите страницу свойств **Свойства конфигурации**  >  **C/C++**  >  **Командная строка** .

1. Введите параметр компилятора в поле **Дополнительные параметры** .

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
