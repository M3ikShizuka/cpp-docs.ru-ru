---
description: 'Дополнительные сведения: два способа создания объекта CArchive'
title: Два способа создать объект CArchive
ms.date: 11/04/2016
helpviewer_keywords:
- CArchive class [MFC], closing CArchive objects
- CArchive objects [MFC], closing
- I/O [MFC], creating CArchive objects
- serialization [MFC], CArchive class
- CArchive objects [MFC]
- storage [MFC], CArchive class [MFC]
- data storage [MFC], CArchive class
- CArchive class [MFC], constructor
ms.assetid: aefa28ce-b55c-40dc-9e42-5f038030985d
ms.openlocfilehash: 21a4321eef2d93cf0b37d157f57e12fa1ba940c8
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97263859"
---
# <a name="two-ways-to-create-a-carchive-object"></a>Два способа создать объект CArchive

Существует два способа создания `CArchive` объекта.

- [Неявное создание объекта CArchive через платформу](#_core_implicit_creation_of_a_carchive_object_via_the_framework)

- [Явное создание объекта CArchive](#_core_explicit_creation_of_a_carchive_object)

## <a name="implicit-creation-of-a-carchive-object-via-the-framework"></a><a name="_core_implicit_creation_of_a_carchive_object_via_the_framework"></a> Неявное создание объекта CArchive через платформу

Самый распространенный и простой способ — позволить платформе создать `CArchive` объект для документа от имени команд Сохранить, сохранить как и открыть в меню файл.

Ниже показано, что делает платформа, когда пользователь приложения выдает команду "Сохранить как" из меню "файл":

1. Представляет диалоговое окно **Сохранить как** и получает имя файла от пользователя.

1. Открывает файл с именем пользователя в качестве `CFile` объекта.

1. Создает `CArchive` объект, указывающий на этот `CFile` объект. При создании `CArchive` объекта платформа устанавливает для режима значение "Store" (запись, сериализация), а не "Load" (чтение, десериализация).

1. Вызывает `Serialize` функцию, определенную в `CDocument` классе, производном от класса, передавая ему ссылку на `CArchive` объект.

`Serialize`Затем функция документа записывает данные в `CArchive` объект, как описано ниже. После возврата из `Serialize` функции платформа уничтожает `CArchive` объект, а затем `CFile` объект.

Таким же, если вы разрешите платформе создать `CArchive` объект для документа, достаточно реализовать `Serialize` функцию документа, которая осуществляет запись и чтение архива. Также необходимо реализовать `Serialize` для `CObject` объектов, производных от, которые `Serialize` функция документа в свою очередь сериализует напрямую или косвенно.

## <a name="explicit-creation-of-a-carchive-object"></a><a name="_core_explicit_creation_of_a_carchive_object"></a> Явное создание объекта CArchive

Помимо сериализации документа с помощью платформы существуют и другие случаи, когда может потребоваться `CArchive` объект. Например, может потребоваться сериализовать данные в буфер обмена и из него, представленные `CSharedFile` объектом. Или же можно использовать пользовательский интерфейс для сохранения файла, отличающегося от платформы, предлагаемой платформой. В этом случае можно явно создать `CArchive` объект. Это выполняется так же, как платформа, с помощью следующей процедуры.

#### <a name="to-explicitly-create-a-carchive-object"></a>Явное создание объекта CArchive

1. Создайте `CFile` объект или объект, производный от `CFile` .

1. Передайте `CFile` объект в конструктор для `CArchive` , как показано в следующем примере:

   [!code-cpp[NVC_MFCSerialization#5](../mfc/codesnippet/cpp/two-ways-to-create-a-carchive-object_1.cpp)]

   Вторым аргументом `CArchive` конструктора является перечислимое значение, которое указывает, будет ли Архив использоваться для хранения или загрузки данных в файл или из него. `Serialize`Функция объекта проверяет это состояние, вызывая `IsStoring` функцию для объекта архива.

Завершив сохранение или загрузку данных в объект или из него `CArchive` , закройте его. Хотя `CArchive` объекты (и `CFile` ) автоматически закрывают Архив (и файл), рекомендуется явно сделать это, так как он упрощает восстановление из-за ошибок. Дополнительные сведения об обработке ошибок см. в статье [исключения: перехват и удаление исключений](../mfc/exceptions-catching-and-deleting-exceptions.md).

#### <a name="to-close-the-carchive-object"></a>Закрытие объекта CArchive

1. В следующем примере показано, как закрыть `CArchive` объект:

   [!code-cpp[NVC_MFCSerialization#6](../mfc/codesnippet/cpp/two-ways-to-create-a-carchive-object_2.cpp)]

## <a name="see-also"></a>См. также раздел

[Сериализация: сериализация объекта](../mfc/serialization-serializing-an-object.md)
