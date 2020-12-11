---
description: 'Дополнительные сведения: Добавление простого объекта ATL'
title: Добавление простого объекта ATL
ms.date: 11/04/2016
f1_keywords:
- vc.codewiz.classes.adding.atl
helpviewer_keywords:
- ATL projects, adding objects
- objects [ATL]
- ATL, simple objects
ms.assetid: 9c57d2ef-0447-4c84-8982-3304b8e49847
ms.openlocfilehash: 9e354f7d361c64f20657190bc53696f9878fa134
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97158940"
---
# <a name="adding-an-atl-simple-object"></a>Добавление простого объекта ATL

Чтобы добавить в проект объект ATL (библиотека активных шаблонов), проект должен быть создан как приложение ATL или как приложение MFC, содержащее поддержку ATL. Можно использовать [Мастер проектов ATL](../../atl/reference/atl-project-wizard.md) для создания приложения ATL или [Добавить объект ATL в приложение MFC](../../mfc/reference/adding-atl-support-to-your-mfc-project.md) для реализации поддержки ATL для приложения MFC.

Вы можете определить COM-интерфейсы для нового объекта ATL при первом создании или добавить их позже с помощью команды [реализовать интерфейс](../../ide/implementing-an-interface-visual-cpp.md#implement-interface-wizard) в контекстном меню **представление классов** .

## <a name="to-add-an-atl-simple-object-to-your-atl-com-project"></a>Добавление простого объекта ATL в проект ATL COM

1. В **Обозреватель решений** или [представление классов](/visualstudio/ide/viewing-the-structure-of-code)щелкните правой кнопкой мыши имя проекта, в который нужно добавить простой объект ATL.

1. В контекстном меню выберите команду **Добавить**, а затем — **Добавить класс**.

1. В диалоговом окне [Добавление класса](../../ide/adding-a-class-visual-cpp.md#add-class-dialog-box) в области **шаблоны** щелкните **простой объект ATL**, а затем нажмите кнопку **Открыть** , чтобы открыть [мастер простых объектов ATL](../../atl/reference/atl-simple-object-wizard.md).

1. Задайте дополнительные параметры для проекта на странице [Параметры](../../atl/reference/options-atl-simple-object-wizard.md) мастера **простых объектов ATL** .

1. Нажмите кнопку **Готово** , чтобы добавить объект в проект.

## <a name="see-also"></a>См. также раздел

[Добавление класса](../../ide/adding-a-class-visual-cpp.md)<br/>
[Добавление нового интерфейса в проект ATL](../../atl/reference/adding-a-new-interface-in-an-atl-project.md)<br/>
[Добавление точек подключения к объекту](../../atl/adding-connection-points-to-an-object.md)<br/>
[Добавление метода](../../ide/adding-a-method-visual-cpp.md)<br/>
[Класс MFC](../../mfc/reference/adding-an-mfc-class.md)<br/>
[Добавление универсального класса C++](../../ide/adding-a-generic-cpp-class.md)
