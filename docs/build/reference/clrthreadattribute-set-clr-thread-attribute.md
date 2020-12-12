---
description: Дополнительные сведения о:/CLRTHREADATTRIBUTE (Установка атрибута потока CLR)
title: /CLRTHREADATTRIBUTE (Установка атрибута потока среды CLR)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.CLRThreadAttribute
helpviewer_keywords:
- /CLRTHREADATTRIBUTE linker option
- -CLRTHREADATTRIBUTE linker option
ms.assetid: 4907e9ef-5031-446c-aecf-0a0b32fae1e8
ms.openlocfilehash: 119797ee10ed0c08477b8e08635605e4299ffd41
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97179126"
---
# <a name="clrthreadattribute-set-clr-thread-attribute"></a>/CLRTHREADATTRIBUTE (Установка атрибута потока среды CLR)

Явно укажите атрибут потоковой обработки для точки входа программы CLR.

## <a name="syntax"></a>Синтаксис

```
/CLRTHREADATTRIBUTE:{STA|MTA|NONE}
```

#### <a name="parameters"></a>Параметры

**MTA**<br/>
Применяет атрибут MTAThreadAttribute к точке входа программы.

**NONE**<br/>
То же, что и без указания/КЛРСРЕАДАТТРИБУТЕ.  Позволяет среде CLR задавать потоковый атрибут по умолчанию.

**STA**<br/>
Применяет атрибут STAThreadAttribute к точке входа программы.

## <a name="remarks"></a>Комментарии

Установка атрибута Thread допустима только при сборке EXE-файла, так как она влияет на точку входа основного потока.

При использовании точки входа по умолчанию (например, Main или wmain) укажите модель потоков с помощью/CLRTHREADATTRIBUTE или поместив атрибут Threading (STAThreadAttribute или MTAThreadAttribute) в функцию ввода по умолчанию.

Если используется точка входа, не используемая по умолчанию, укажите потоковую модель либо с помощью/CLRTHREADATTRIBUTE, либо поместив атрибут Threading в функцию записи, не используемую по умолчанию, а затем укажите точку входа, не используемую по умолчанию, с параметром [/entry](entry-entry-point-symbol.md).

Если потоковая модель, указанная в исходном коде, не согласуется с потоковой моделью, заданной с помощью/CLRTHREADATTRIBUTE, компоновщик будет игнорировать/CLRTHREADATTRIBUTE и применить потоковую модель, указанную в исходном коде.

Например, если в вашей программе CLR размещается COM-объект, использующий однопотоковое приложение, то потребуется использовать однопотоковое.  Если ваша программа CLR использует многопоточность, она не может разместить COM-объект, использующий однопотоковое управление.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Задание данного параметра компоновщика в среде разработки Visual Studio

1. Откройте диалоговое окно **Страницы свойств** проекта. Подробнее см. в статье [Настройка компилятора C++ и свойства сборки в Visual Studio](../working-with-project-properties.md).

1. Разверните узел **Свойства конфигурации**.

1. Разверните узел **Компоновщик**.

1. Выберите страницу свойств **Дополнительно**.

1. Измените свойство **атрибута потока среды CLR** .

### <a name="to-set-this-linker-option-programmatically"></a>Задание данного параметра компоновщика программным способом

1. См. раздел <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.CLRThreadAttribute%2A>.

## <a name="see-also"></a>См. также раздел

[Справочник по компоновщику MSVC](linking.md)<br/>
[Параметры компоновщика MSVC](linker-options.md)
