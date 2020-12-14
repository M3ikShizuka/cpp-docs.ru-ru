---
description: Дополнительные сведения о команде:/ENTRY (символ точки входа)
title: /ENTRY (символ точки входа)
ms.date: 11/04/2016
f1_keywords:
- /entry
- VC.Project.VCLinkerTool.EntryPointSymbol
helpviewer_keywords:
- starting address
- -ENTRY linker option
- /ENTRY linker option
- ENTRY linker option
ms.assetid: 26c62ba2-4f52-4882-a7bd-7046a0abf445
ms.openlocfilehash: e4966ef44922a3a90d5abb5a7ac23460d4155f92
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97201018"
---
# <a name="entry-entry-point-symbol"></a>/ENTRY (символ точки входа)

```
/ENTRY:function
```

## <a name="arguments"></a>Аргументы

*function*<br/>
Функция, указывающая определяемый пользователем начальный адрес для EXE-файла или библиотеки DLL.

## <a name="remarks"></a>Комментарии

Параметр/ENTRY задает функцию точки входа в качестве начального адреса для EXE-файла или библиотеки DLL.

Для использования **`__stdcall`** соглашения о вызовах функция должна быть определена. Параметры и возвращаемое значение зависят от того, является ли программа консольным приложением, приложением Windows или библиотекой DLL. Рекомендуется позволить компоновщику установить точку входа таким образом, чтобы библиотека времени выполнения языка C была инициализирована правильно, а также выполнялись конструкторы C++ для статических объектов.

По умолчанию начальный адрес — это имя функции из библиотеки времени выполнения языка C. Компоновщик выбирает его в соответствии с атрибутами программы, как показано в следующей таблице.

|Имя функции|По умолчанию для|
|-------------------|-----------------|
|**mainCRTStartup** (или **вмаинкртстартуп**)|Приложение, использующее/SUBSYSTEM: CONSOLE; вызовы `main` (или `wmain` )|
|**Винмаинкртстартуп** (или **ввинмаинкртстартуп**)|Приложение, использующее/SUBSYSTEM:**Windows**; вызовы `WinMain` (или `wWinMain` ), которые должны быть определены для использования **`__stdcall`**|
|**_DllMainCRTStartup**|DLL; вызывает `DllMain` , если он существует, который должен быть определен для использования **`__stdcall`**|

Если параметр [/DLL](dll-build-a-dll.md) или [/SUBSYSTEM](subsystem-specify-subsystem.md) не указан, компоновщик выбирает подсистему и точку входа в зависимости от того, `main` `WinMain` определено ли значение.

Функции `main` , `WinMain` и `DllMain` являются тремя формами пользовательской точки входа.

При создании управляемого образа функция, указанная в/ENTRY, должна иметь сигнатуру (ЛПВОИД *var1*, DWORD *var2*, лпвоид *var3*).

Сведения о том, как определить собственную `DllMain` точку входа, см. в разделе [dll и Visual C++ поведение библиотеки времени выполнения](../run-time-library-behavior.md) .

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Выберите папку **компоновщика**.

1. Перейдите на страницу свойств **Дополнительно** .

1. Измените свойство **точки входа** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

- См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.EntryPointSymbol%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
