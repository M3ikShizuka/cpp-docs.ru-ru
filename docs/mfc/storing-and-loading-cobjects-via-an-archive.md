---
description: Дополнительные сведения см. в статье хранение и загрузка CObjects через архив.
title: Сохранение и загрузка CObjects через архив
ms.date: 11/04/2016
helpviewer_keywords:
- CObjects [MFC], loading through archives
- CArchive class [MFC], storing and loading objects
- Serialize method, vs. CArchive operators
- CObject class [MFC], CArchive objects
- CObjects [MFC]
ms.assetid: a829b6dd-bc31-47e0-8108-fbb946722db9
ms.openlocfilehash: c84c507fc556268eea526c1350211fd4b82f54fe
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97216565"
---
# <a name="storing-and-loading-cobjects-via-an-archive"></a>Сохранение и загрузка CObjects через архив

Хранение и загрузка `CObject` с помощью архива требует дополнительного рассмотрения. В некоторых случаях следует вызывать `Serialize` функцию объекта, где `CArchive` объект является параметром `Serialize` вызова, а не с помощью **<\<** or **>>** оператора класса `CArchive` . Важно помнить, что `CArchive` **>>** оператор конструирует `CObject` в памяти на основе `CRuntimeClass` сведений, записанных в файл архивом хранения.

Таким образом, если вы используете `CArchive` **<\<** and **>>** операторы и вызов `Serialize` , зависит от того, *нужен* ли Архив загрузки для динамической реконструирования объекта на основе ранее сохраненной `CRuntimeClass` информации. Используйте `Serialize` функцию в следующих случаях:

- При десериализации объекта необходимо заранее понять точный класс объекта.

- При десериализации объекта для него уже выделяется память.

> [!CAUTION]
> При загрузке объекта с помощью `Serialize` функции необходимо также сохранить объект с помощью `Serialize` функции. Не сохраняйте с помощью `CArchive` **<<** оператора, затем загрузите с помощью `Serialize` функции или сохраните с помощью `Serialize` функции, а затем загрузите `CArchive >>` оператор using.

В следующем примере показаны варианты:

[!code-cpp[NVC_MFCSerialization#36](../mfc/codesnippet/cpp/storing-and-loading-cobjects-via-an-archive_1.h)]

[!code-cpp[NVC_MFCSerialization#37](../mfc/codesnippet/cpp/storing-and-loading-cobjects-via-an-archive_2.cpp)]

В целом, если сериализуемый класс определяет внедренный в `CObject` качестве члена, *не* следует использовать `CArchive` **<\<** and **>>** операторы для этого объекта, но следует вызывать `Serialize` функцию. Кроме того, если сериализуемый класс определяет указатель на `CObject` (или объект, производный от `CObject` ) в качестве члена, но конструирует этот другой объект в собственном конструкторе, следует также вызвать метод `Serialize` .

## <a name="see-also"></a>См. также раздел

[Сериализация: сериализация объекта](../mfc/serialization-serializing-an-object.md)
