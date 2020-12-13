---
description: 'Дополнительные сведения: Создание шаблона документа'
title: Создание шаблонов документов
ms.date: 11/04/2016
helpviewer_keywords:
- document templates [MFC]
- constructors [MFC], document template
- document templates [MFC], creating
- MFC, document templates
- templates [MFC], document templates
ms.assetid: c87f1821-7cbf-442e-9690-f126ae7fb783
ms.openlocfilehash: 60f85cf0a1c16e1aaa6057160c5b986001e18d84
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330266"
---
# <a name="document-template-creation"></a>Создание шаблонов документов

При создании нового документа в ответ на команду **создать** или **Открыть** в меню **файл** шаблон документа также создает новое окно фрейма, в котором можно просмотреть документ.

Конструктор шаблона документа определяет типы документов, окон и представлений, которые шаблон может создать. Это определяется аргументами, передаваемыми конструктору шаблона документа. Следующий код иллюстрирует создание [кмултидоктемплате](reference/cmultidoctemplate-class.md) для примера приложения:

[!code-cpp[NVC_MFCDocView#7](codesnippet/cpp/document-template-creation_1.cpp)]

Указатель на новый `CMultiDocTemplate` объект используется в качестве аргумента для [AddDocTemplate](reference/cwinapp-class.md#adddoctemplate). Аргументы `CMultiDocTemplate` конструктора включают идентификатор ресурса, связанный с меню и ускорителями типа документа, и три применения макроса [RUNTIME_CLASS](reference/run-time-object-model-services.md#runtime_class) . `RUNTIME_CLASS` Возвращает объект [крунтимекласс](reference/cruntimeclass-structure.md) для класса C++ с именем в качестве аргумента. Три `CRuntimeClass` объекта, передаваемые конструктору шаблона документа, предоставляют сведения, необходимые для создания новых объектов указанных классов в процессе создания документа. В примере показано создание шаблона документа, который создает `CScribDoc` объекты с `CScribView` присоединенными объектами. Представления выделяются стандартными окнами дочернего фрейма MDI.

## <a name="see-also"></a>См. также раздел

[Шаблоны документов и процесс создания документа/представления](document-templates-and-the-document-view-creation-process.md)<br/>
[Создание документа или представления](document-view-creation.md)<br/>
[Связи между объектами MFC](relationships-among-mfc-objects.md)<br/>
[Создание новых документов, окон и представлений](creating-new-documents-windows-and-views.md)
