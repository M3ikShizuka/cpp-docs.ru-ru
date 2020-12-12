---
description: 'Дополнительные сведения: @ (укажите файл ответов компилятора)'
title: '@ (указать файл ответа компилятора)'
ms.date: 11/04/2016
f1_keywords:
- '@'
helpviewer_keywords:
- response files, C/C++ compiler
- '@ compiler option'
- cl.exe compiler, specifying response files
ms.assetid: 400fffee-909d-4f60-bf76-45833e822685
ms.openlocfilehash: bd2859f7973723d93594693902e92ac3530d73ff
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97182896"
---
# <a name="-specify-a-compiler-response-file"></a>@ (указать файл ответа компилятора)

Указывает файл ответов компилятора.

## <a name="syntax"></a>Синтаксис

> **\@**<em>response_file</em>

## <a name="arguments"></a>Аргументы

*response_file*<br/>
Текстовый файл, содержащий команды компилятора.

## <a name="remarks"></a>Комментарии

Файл ответов может содержать любые команды, указанные в командной строке. Это может быть полезно, если аргументы командной строки длиннее 127 символов.

Невозможно указать **\@** параметр в файле ответов. То есть файл ответов не может внедрить другой файл ответов.

В командной строке можно указать любое количество параметров файла ответа (например, `@respfile.1 @respfile.2` ).

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Установка данного параметра компилятора в среде разработки Visual Studio

- Файл ответов не может быть указан в среде разработки и должен быть указан в командной строке.

### <a name="to-set-this-compiler-option-programmatically"></a>Установка данного параметра компилятора программным способом

- Этот параметр компилятора нельзя изменить программным способом.

## <a name="see-also"></a>См. также раздел

[Параметры компилятора MSVC](compiler-options.md)<br/>
[Синтаксис Command-Line компилятора КОМПИЛЯТОРОМ MSVC](compiler-command-line-syntax.md)
