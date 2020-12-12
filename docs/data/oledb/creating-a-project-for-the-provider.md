---
description: 'Дополнительные сведения: Создание проекта для поставщика'
title: Создание проекта для поставщика
ms.date: 10/22/2018
helpviewer_keywords:
- ATL projects, creating
- OLE DB providers, projects
- projects [C++], creating
ms.assetid: 076a75de-1d4b-486a-bcf8-9c0f6b049fa2
ms.openlocfilehash: 9094e4bfc57838425793fac0c009ed70259dcb3a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323250"
---
# <a name="creating-a-project-for-the-provider"></a>Создание проекта для поставщика

## <a name="to-create-a-project-in-which-the-ole-db-provider-will-reside"></a>Создание проекта, в котором будет располагаться поставщик OLE DB

1. В меню **Файл** последовательно выберите пункты **Создать** и **Проект**.

   Откроется диалоговое окно **Новый проект** .

1. В области **типы проектов** щелкните **установленную**  >  **Visual C++**  >  папку **MFC/ATL** . В области **шаблоны** щелкните **проект ATL**.

    > [!NOTE]
    > В предыдущих версиях Visual Studio найдите тип проекта в разделе **установленные**  >  **шаблоны**  >  **Visual C++**  >  **ATL**.

1. В поле **имя** введите имя проекта и нажмите кнопку **ОК**.

   Откроется **Мастер проектов ATL** .

1. В **мастере проектов ATL** выберите **Библиотека динамической компоновки (DLL)** для **типа приложения**.

1. Нажмите кнопку **Готово**.

## <a name="see-also"></a>См. также раздел

[Создание поставщика OLE DB](../../data/oledb/creating-an-ole-db-provider.md)
