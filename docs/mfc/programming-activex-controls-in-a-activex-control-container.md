---
description: 'Дополнительные сведения см. в статье контейнеры элементов управления ActiveX: Программирование элементов управления ActiveX в контейнере элементов управления ActiveX.'
title: Контейнеры элементов управления ActiveX. Программирование элементов управления ActiveX в контейнере элементов управления ActiveX
ms.date: 09/12/2018
helpviewer_keywords:
- ActiveX control containers [MFC], accessing ActiveX controls
- Confirm Classes dialog box
- wrapper classes [MFC], ActiveX controls
- ActiveX control containers [MFC], wrapper classes
- ActiveX controls [MFC], accessing
- MFC ActiveX controls [MFC], accessing in containers
- header files [MFC], for ActiveX control wrapper class
- wrapper classes [MFC], using
- ActiveX controls [MFC], wrapper classes
ms.assetid: ef9b2480-92d6-4191-b16e-8055c4fd7b73
ms.openlocfilehash: 34a5a2aaa1d7ec940ea31ae2fbe8c89ba3d84818
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97251015"
---
# <a name="activex-control-containers-programming-activex-controls-in-an-activex-control-container"></a>Контейнеры элементов управления ActiveX. Программирование элементов управления ActiveX в контейнере элементов управления ActiveX

В этой статье описывается процесс доступа к предоставленным [методам](../mfc/mfc-activex-controls-methods.md) и [свойствам](../mfc/mfc-activex-controls-properties.md) внедренных элементов управления ActiveX.

>[!IMPORTANT]
> ActiveX — это устаревшая технология, которую не следует использовать для новой разработки. Дополнительные сведения о современных технологиях, которые заменяют ActiveX, см. в разделе [элементы управления ActiveX](activex-controls.md).

По сути, необходимо выполнить следующие действия.

1. [Вставка элемента управления ActiveX в проект контейнера ActiveX](../mfc/inserting-a-control-into-a-control-container-application.md) с помощью коллекции.

1. [Определите переменную-член](../mfc/activex-control-containers-connecting-an-activex-control-to-a-member-variable.md) (или другую форму доступа) того же типа, что и класс-оболочка элемента управления ActiveX.

1. [Программирование элемента управления ActiveX](#_core_programming_the_activex_control) с помощью стандартных функций-членов класса-оболочки.

В этом обсуждении предполагается, что вы создали проект на основе диалогового окна (именованный контейнер) с поддержкой элементов управления ActiveX. В результирующий проект будет добавлен пример элемента управления Circ, Circ.

После вставки элемента управления Circ в проект (шаг 1) вставьте экземпляр элемента управления Circ в главное диалоговое окно приложения.

## <a name="procedures"></a>Процедуры

#### <a name="to-add-the-circ-control-to-the-dialog-template"></a>Добавление элемента управления Circ в шаблон диалогового окна

1. Загрузите проект контейнера элемента управления ActiveX. В этом примере используйте `Container` проект.

1. Перейдите на вкладку представление ресурсов.

1. Откройте папку **диалогового окна** .

1. Дважды щелкните шаблон главного диалогового окна. В этом примере используйте **IDD_CONTAINER_DIALOG**.

1. Щелкните значок элемента управления Circ на панели элементов.

1. Щелкните место в диалоговом окне, чтобы вставить элемент управления Circ.

1. В меню **файл** выберите команду **сохранить все** , чтобы сохранить все изменения в шаблоне диалогового окна.

## <a name="modifications-to-the-project"></a>Изменения в проекте

Чтобы разрешить приложению-контейнеру доступ к элементу управления Circ, Visual C++ автоматически добавляет файл реализации класса-оболочки ( `CCirc` ) (. CPP) в проект контейнера и в заголовок класса-оболочки (. H) файл заголовка диалогового окна:

[!code-cpp[NVC_MFC_AxCont#1](../mfc/codesnippet/cpp/programming-activex-controls-in-a-activex-control-container_1.h)]

## <a name="the-wrapper-class-header-h-file"></a><a name="_core_the_wrapper_class_header_28h29_file"></a> Заголовок класса-оболочки (. H) файл

Для получения и задания свойств (и вызова методов) для элемента управления Circ класс- `CCirc` оболочка предоставляет объявление всех предоставляемых методов и свойств. В этом примере эти объявления находятся в CIRC. H. В следующем примере показана часть класса `CCirc` , определяющая предоставляемые интерфейсы элемента управления ActiveX:

[!code-cpp[NVC_MFC_AxCont#2](../mfc/codesnippet/cpp/programming-activex-controls-in-a-activex-control-container_2.h)]
[!code-cpp[NVC_MFC_AxCont#3](../mfc/codesnippet/cpp/programming-activex-controls-in-a-activex-control-container_3.h)]

Затем эти функции могут быть вызваны из других процедур приложения с помощью обычного синтаксиса C++. Дополнительные сведения об использовании этого набора функций элементов для доступа к методам и свойствам элемента управления см. в разделе [Программирование элемента управления ActiveX](#_core_programming_the_activex_control).

## <a name="member-variable-modifications-to-the-project"></a><a name="_core_member_variable_modifications_to_the_project"></a> Изменения переменных членов в проекте

После того как элемент управления ActiveX добавлен в проект и внедрен в контейнер диалогового окна, доступ к нему могут получить другие части проекта. Самый простой способ получить доступ к элементу управления — [создать переменную-член](../mfc/activex-control-containers-connecting-an-activex-control-to-a-member-variable.md) класса диалогового окна `CContainerDlg` (шаг 2), который относится к тому же типу, что и класс-оболочка, добавленный в проект Visual C++. Затем можно использовать переменную члена для доступа к внедренному элементу управления в любое время.

Когда диалоговое окно **Добавление переменной-члена** добавляет в проект переменную-член *m_circctl* , она также добавляет следующие строки в файл заголовка (. H) `CContainerDlg` класса:

[!code-cpp[NVC_MFC_AxCont#4](../mfc/codesnippet/cpp/programming-activex-controls-in-a-activex-control-container_4.h)]
[!code-cpp[NVC_MFC_AxCont#5](../mfc/codesnippet/cpp/programming-activex-controls-in-a-activex-control-container_5.h)]

Кроме того, вызов **DDX_Control** автоматически добавляется в `CContainerDlg` реализацию `DoDataExchange` :

[!code-cpp[NVC_MFC_AxCont#6](../mfc/codesnippet/cpp/programming-activex-controls-in-a-activex-control-container_6.cpp)]

## <a name="programming-the-activex-control"></a><a name="_core_programming_the_activex_control"></a> Программирование элемента управления ActiveX

На этом этапе вы вставили элемент управления ActiveX в шаблон диалогового окна и создали для него переменную-член. Теперь можно использовать общий синтаксис C++ для доступа к свойствам и методам внедренного элемента управления.

Как отмечалось (в [заголовке класса-оболочки (. H)](#_core_the_wrapper_class_header_28h29_file)— файл заголовка (. H) для `CCirc` класса-оболочки, в данном случае это Circ. H содержит список функций-членов, которые можно использовать для получения и задания любого значения предоставленного свойства. Также доступны функции элементов для предоставляемых методов.

Распространенным местом для изменения свойств элемента управления является `OnInitDialog` функция-член основного класса диалогового окна. Эта функция вызывается непосредственно перед отображением диалогового окна и используется для инициализации его содержимого, включая все элементы управления.

В следующем примере кода используется переменная члена *m_circctl* для изменения свойств Caption и Цирклешапе внедренного элемента управления Circ:

[!code-cpp[NVC_MFC_AxCont#7](../mfc/codesnippet/cpp/programming-activex-controls-in-a-activex-control-container_7.cpp)]

## <a name="see-also"></a>См. также раздел

[Контейнеры элементов управления ActiveX](../mfc/activex-control-containers.md)
