---
description: 'Дополнительные сведения: регистрация классов окон'
title: Регистрация классов Window
ms.date: 11/04/2016
f1_keywords:
- WndProc
helpviewer_keywords:
- window classes [MFC], registering
- registry [MFC], registering classes
- AfxRegisterWndClass method [MFC]
- MFC, windows
- WinMain method [MFC], and registering window classes
- WndProc method [MFC]
- classes [MFC], registering window classes
- WinMain method [MFC]
- registering window classes [MFC]
ms.assetid: 30994bc4-a362-43da-bcc5-1bf67a3fc929
ms.openlocfilehash: e31f83b691ad12d845afca6a3a5f18d9ba64b0e6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97218196"
---
# <a name="registering-window-classes"></a>Регистрация классов Window

Окно "классы" в традиционном программировании для Windows определяют характеристики "класса" (не класс C++), из которого можно создать любое количество окон. Этот тип класса является шаблоном или моделью для создания окон.

## <a name="window-class-registration-in-traditional-programs-for-windows"></a>Регистрация класса окна в традиционных программах для Windows

В традиционной программе для Windows, без MFC, все сообщения обрабатываются в окне в его «процедуре окна» или « `WndProc` .» Объект `WndProc` связан с окном с помощью процесса регистрации класса окна. Главное окно регистрируется в `WinMain` функции, но другие классы Windows можно зарегистрировать в любом месте приложения. Регистрация зависит от структуры, содержащей указатель на `WndProc` функцию вместе с спецификациями курсора, фоновой кисти и т. д. Структура передается в качестве параметра вместе с строковым именем класса в предыдущем вызове `RegisterClass` функции. Таким же класс регистрации может совместно использоваться несколькими окнами.

## <a name="window-class-registration-in-mfc-programs"></a>Регистрация класса окна в программах MFC

В отличие от этого, большинство действий по регистрации класса Window выполняется автоматически в программе платформы MFC. При использовании MFC обычно создается класс окна C++ из существующего класса библиотеки с помощью обычного синтаксиса C++ для наследования класса. Платформа по-прежнему использует традиционные "классы регистрации" и предоставляет несколько стандартных, зарегистрированных для вас при необходимости. Можно зарегистрировать дополнительные классы регистрации, вызвав глобальную функцию [афксрегистервндкласс](../mfc/reference/application-information-and-management.md#afxregisterwndclass) , а затем передав зарегистрированный класс в `Create` функцию члена `CWnd` . Как описано здесь, традиционный "класс регистрации" в Windows не следует путать с классом C++.

Дополнительные сведения см. в [техническом примечании 1](../mfc/tn001-window-class-registration.md).

## <a name="see-also"></a>См. также раздел

[Создание Windows](../mfc/creating-windows.md)
