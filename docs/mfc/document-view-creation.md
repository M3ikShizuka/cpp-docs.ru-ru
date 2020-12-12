---
description: 'Дополнительные сведения: создание документа или представления'
title: Создание Document-View
ms.date: 11/04/2016
helpviewer_keywords:
- documents [MFC], creating
- views [MFC], and frame windows
- views [MFC], creating
- tables [MFC]
- MFC, views
- document/view architecture [MFC], creating document/view
- object creators
- MFC, documents
- tables [MFC], objects each MFC object creates
ms.assetid: bda14f41-ed50-439d-af9e-591174e7dd64
ms.openlocfilehash: 128b68eb53bd596ba2e4b4df4f2c5e865452fe2a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97326439"
---
# <a name="documentview-creation"></a>Создание документа или представления

Платформа предоставляет реализации команд **New** и **Open** (из других) в меню **файл** . Создание нового документа и связанного с ним представления и окна фрейма — это совместная работа между объектом приложения, шаблоном документа, вновь созданным документом и вновь созданным окном фрейма. В следующей таблице приводятся сводные сведения о том, какие объекты создают.

### <a name="object-creators"></a>Создатели объектов

|Автор|Приводит|
|-------------|-------------|
|Объект приложения|Шаблон документа|
|Шаблон документа|Документ|
|Шаблон документа|Окно фрейма|
|Окно фрейма|Представление|

## <a name="see-also"></a>См. также раздел

[Шаблоны документов и процесс создания документа/представления](document-templates-and-the-document-view-creation-process.md)<br/>
[Создание шаблона документа](document-template-creation.md)<br/>
[Связи между объектами MFC](relationships-among-mfc-objects.md)<br/>
[Создание новых документов, окон и представлений](creating-new-documents-windows-and-views.md)
