---
description: Дополнительные сведения см. в статье поддержка MFC в проектах ATL.
title: Поддержка MFC в проектах ATL
ms.date: 11/04/2016
f1_keywords:
- vc.atl.addmfc
helpviewer_keywords:
- ATL projects, MFC support
ms.assetid: f90b4276-cb98-4c11-902c-9ebcfe6f954b
ms.openlocfilehash: 8614bfdd5320e0ecdf34cc96251fa8a20f2dede9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97157923"
---
# <a name="mfc-support-in-atl-projects"></a>Поддержка MFC в проектах ATL

При выборе **поддержки MFC** в мастере проектов ATL проект объявляет приложение как объект приложения MFC (класс). Проект инициализирует библиотеку MFC и создает экземпляр класса (класс *ProjName*), производный от [CWinApp](../../mfc/reference/cwinapp-class.md).

Этот параметр доступен только для проектов ATL DLL без атрибутов.

```
class CProjNameApp : public CWinApp
{
public:

// Overrides
    virtual BOOL InitInstance();
virtual int ExitInstance();
DECLARE_MESSAGE_MAP()
};

BEGIN_MESSAGE_MAP(CProjNameApp, CWinApp)
END_MESSAGE_MAP()

CProjNameApp theApp;

BOOL CProjNameApp::InitInstance()
{
    return CWinApp::InitInstance();

}

int CProjNameApp::ExitInstance()
{
    return CWinApp::ExitInstance();

}
```

Можно просмотреть класс объекта приложения и его `InitInstance` `ExitInstance` функции и в представление классов.

## <a name="see-also"></a>См. также раздел

[Добавление класса](../../ide/adding-a-class-visual-cpp.md)<br/>
[Создание проекта ATL](../../atl/reference/creating-an-atl-project.md)<br/>
[Конфигурации проектов ATL по умолчанию](../../atl/reference/default-atl-project-configurations.md)
