---
description: 'Дополнительные сведения о: Диспетчер визуализации'
title: Диспетчер визуализации
ms.date: 11/19/2018
helpviewer_keywords:
- Visualization Manager
ms.assetid: c9dd1365-27ac-42e5-8caa-1004525b4129
ms.openlocfilehash: b99331503e4e7e69cc5d8a19fde7641c1b1daeeb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97143212"
---
# <a name="visualization-manager"></a>Диспетчер визуализации

Визуальный диспетчер — это объект, управляющий внешним видом всего приложения. Он выступает в качестве одного класса, в котором можно разместить весь код рисования приложения. Библиотека MFC содержит несколько визуальных руководителей. Вы также можете создать собственный визуальный диспетчер, если вы хотите создать пользовательское представление для приложения. На следующих изображениях показано одно и то же приложение при включении различных диспетчеров визуальных элементов.

![MyApp, преобразованный CMFCVisualManagerWindows](../mfc/media/vmwindows.png "MyApp, преобразованный CMFCVisualManagerWindows") <br/>
MyApp, использующий визуальный диспетчер Кмфквисуалманажервиндовс

![MyApp, преобразованный CMFCVisualManagerVS2005](../mfc/media/vmvs2005.png "MyApp, преобразованный CMFCVisualManagerVS2005") <br/>
MyApp, использующий визуальный диспетчер CMFCVisualManagerVS2005

![MyApp, преобразованный CMFCVisualManagerOfficeXP](../mfc/media/vmofficexp.png "MyApp, преобразованный CMFCVisualManagerOfficeXP") <br/>
MyApp, использующий визуальный диспетчер CMFCVisualManagerOfficeXP

![MyApp, преобразованный CMFCVisualManagerOffice2003](../mfc/media/vmoffice2003.png "MyApp, преобразованный CMFCVisualManagerOffice2003") <br/>
MyApp, использующий визуальный диспетчер CMFCVisualManagerOffice2003

![MyApp, преобразованный CMFCVisualManagerOffice2007](../mfc/media/msoffice2007.png "MyApp, преобразованный CMFCVisualManagerOffice2007") <br/>
MyApp, использующий визуальный диспетчер CMFCVisualManagerOffice2007

По умолчанию визуальный диспетчер поддерживает код рисования для нескольких элементов графического пользовательского интерфейса. Чтобы предоставить настраиваемые элементы пользовательского интерфейса, необходимо переопределить соответствующие методы рисования визуального элемента управления. Список этих методов см. в разделе [Класс CMFCVisualManager](../mfc/reference/cmfcvisualmanager-class.md). Методы, которые можно переопределить для предоставления пользовательского внешнего вида, — это все методы, которые начинаются с `OnDraw` .

Приложение может иметь только один `CMFCVisualManager` объект. Чтобы получить указатель на визуальный диспетчер для приложения, вызовите статическую функцию [CMFCVisualManager::-instance](../mfc/reference/cmfcvisualmanager-class.md#getinstance). Поскольку все визуальные руководители наследуют от `CMFCVisualManager` , `CMFCVisualManager::GetInstance` метод получает указатель на соответствующий Диспетчер визуальных элементов, даже если вы создаете пользовательский визуальный диспетчер.

Если вы хотите создать настраиваемый диспетчер визуальных элементов, необходимо наследовать его от уже существующего визуального диспетчера. Класс по умолчанию, производный от, имеет значение `CMFCVisualManager` . Однако можно использовать другой визуальный диспетчер, если он лучше похож на то, что требуется для приложения. Например, если вы хотите использовать `CMFCVisualManagerOffice2007` Диспетчер визуальных элементов, но хотели только изменить вид разделителей, Пользовательский класс можно создать из `CMFCVisualManagerOffice2007` . В этом сценарии следует перезаписывать только методы для разделителей рисования.

Существует два возможных способа использования конкретного визуального диспетчера для вашего приложения. Один из способов — вызвать метод [CMFCVisualManager:: сетдефаултманажер](../mfc/reference/cmfcvisualmanager-class.md#setdefaultmanager) и передать соответствующий диспетчер визуального элемента в качестве параметра. В следующем примере кода показано, как использовать `CMFCVisualManagerVS2005` визуальный Диспетчер с этим методом:

```cpp
CMFCVisualManager::SetDefaultManager (RUNTIME_CLASS (CMFCVisualManagerVS2005));
```

Другим способом использования визуального диспетчера в приложении является создание его вручную. Затем приложение будет использовать этот новый Диспетчер визуальных элементов для всей отрисовки. Однако, так как в приложении может быть только один `CMFCVisualManager` объект, необходимо удалить текущий диспетчер визуальных элементов перед созданием нового. В следующем примере `CMyVisualManager` — это пользовательский визуальный диспетчер, производный от `CMFCVisualManager` . Следующий метод изменит, какой визуальный диспетчер используется для отображения приложения в зависимости от индекса.

```cpp
void CMyApp::SetSkin (int index)
{
    if (CMFCVisualManager::GetInstance() != NULL)
    {
        delete CMFCVisualManager::GetInstance();
    }

    switch (index)
    {
    case DEFAULT_STYLE:
        // The following statement creates a new CMFCVisualManager
        CMFCVisualManager::GetInstance();
        break;

    case CUSTOM_STYLE:
        new CMyVisualManager;
        break;

    default:
        CMFCVisualManager::GetInstance();
        break;
    }

    CMFCVisualManager::GetInstance()->RedrawAll();
}
```

## <a name="see-also"></a>См. также раздел

[Элементы пользовательского интерфейса](../mfc/user-interface-elements-mfc.md)<br/>
[Класс CMFCVisualManager](../mfc/reference/cmfcvisualmanager-class.md)
