---
description: 'Дополнительные сведения: создание производного класса документа от CDocument'
title: Наследование класса документов от CDocument
ms.date: 11/04/2016
helpviewer_keywords:
- CDocument class [MFC], deriving from
- classes [MFC], deriving from CDocument
- document objects [MFC], derived
- derived classes [MFC], functions often overridden
- document classes [MFC], functions often overridden
ms.assetid: e6a198e0-9799-43c0-83c5-04174d8b532c
ms.openlocfilehash: 9f6dccb5400ba0e62b2f11a3c2d4074cb9bb2f25
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97327885"
---
# <a name="deriving-a-document-class-from-cdocument"></a>Наследование класса документов от CDocument

Документы содержат данные вашего приложения и управляют ими. Чтобы использовать класс документов, предоставляемый мастером приложений MFC, необходимо выполнить следующие действия.

- Создайте класс, производный от, `CDocument` для каждого типа документа.

- Добавьте переменные члена для хранения данных каждого документа.

- Переопределение `CDocument` `Serialize` функции члена в классе документа. `Serialize` записывает и считывает данные документа на диск и обратно.

## <a name="other-document-functions-often-overridden"></a>Другие функции документов, которые часто переопределяются

Также может потребоваться переопределить другие `CDocument` функции элементов. В частности, часто требуется переопределить [онневдокумент](reference/cdocument-class.md#onnewdocument) и [OnOpenDocument](reference/cdocument-class.md#onopendocument) для инициализации элементов данных документа и [делетеконтентс](reference/cdocument-class.md#deletecontents) для уничтожения динамически выделяемых данных. Дополнительные сведения о переопределяемых членах см. в разделе класс [CDocument](reference/cdocument-class.md) в *справочнике по MFC*.

## <a name="see-also"></a>См. также раздел

[Использование документов](using-documents.md)
