---
description: 'Дополнительные сведения: указание уровней функциональности'
title: Задание уровней функциональности
ms.date: 11/06/2018
helpviewer_keywords:
- CObject class [MFC], adding functionality to derived classes
- runtime [MFC], class information
- serialization [MFC], Cobject
- dynamic creation support
- levels [MFC], functionality in CObject
- run-time class [MFC], information support
- levels [MFC]
ms.assetid: 562669ba-c858-4f66-b5f1-b3beeea4f486
ms.openlocfilehash: 1b016cd5a41d3e09790f678a2d49d88df33d9782
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97216851"
---
# <a name="specifying-levels-of-functionality"></a>Задание уровней функциональности

В этой статье описывается, как добавить следующие уровни функциональности в класс, производный от [CObject](../mfc/reference/cobject-class.md):

- Сведения о классе времени выполнения

- Поддержка динамического создания

- Поддержка сериализации

Общее описание `CObject` функциональных возможностей см. в статье [Создание класса, производного от CObject](../mfc/deriving-a-class-from-cobject.md).

## <a name="to-add-run-time-class-information"></a>Добавление сведений о классе времени выполнения

1. Создайте класс, производный от `CObject` , как описано в статье [Создание производного класса от CObject](../mfc/deriving-a-class-from-cobject.md) .

1. Используйте макрос DECLARE_DYNAMIC в объявлении класса, как показано ниже:

   [!code-cpp[NVC_MFCCObjectSample#2](../mfc/codesnippet/cpp/specifying-levels-of-functionality_1.h)]

1. Используйте макрос IMPLEMENT_DYNAMIC в файле реализации (. CPP) класса. Этот макрос принимает в качестве аргументов имя класса и его базовый класс следующим образом:

   [!code-cpp[NVC_MFCCObjectSample#3](../mfc/codesnippet/cpp/specifying-levels-of-functionality_2.cpp)]

> [!NOTE]
> Всегда помещайте IMPLEMENT_DYNAMIC в файл реализации (. CPP) для класса. Макрос IMPLEMENT_DYNAMIC должен вычисляться только один раз во время компиляции, поэтому не должен использоваться в файле интерфейса (. H), которые потенциально могут включаться в несколько файлов.

## <a name="to-add-dynamic-creation-support"></a>Добавление поддержки динамического создания

1. Создайте класс, производный от `CObject` .

1. Используйте макрос DECLARE_DYNCREATE в объявлении класса.

1. Определите конструктор без аргументов (конструктор по умолчанию).

1. Используйте макрос IMPLEMENT_DYNCREATE в файле реализации класса.

## <a name="to-add-serialization-support"></a>Добавление поддержки сериализации

1. Создайте класс, производный от `CObject` .

1. Переопределите `Serialize` функцию члена.

   > [!NOTE]
   > Если вы вызываете `Serialize` напрямую, то есть не хотите сериализовать объект с помощью полиморфизма, пропустите шаги с 3 по 5.

1. Используйте макрос DECLARE_SERIAL в объявлении класса.

1. Определите конструктор без аргументов (конструктор по умолчанию).

1. Используйте макрос IMPLEMENT_SERIAL в файле реализации класса.

> [!NOTE]
> «Одноэлементный указатель» указывает на объект класса (вызовет его) или на объект любого класса, производного от (скажем, B). Чтобы выполнить сериализацию с помощью полиморфизма, платформа должна определить класс времени выполнения для объекта, который он сериализует (B), так как он может быть объектом любого класса, производного от некоторого базового класса (A).

Дополнительные сведения о том, как включить сериализацию при наследовании класса из `CObject` , см. в файлах статей [в MFC и в](../mfc/files-in-mfc.md) разделе [сериализация](../mfc/serialization-in-mfc.md).

## <a name="see-also"></a>См. также раздел

[Наследование класса от CObject](../mfc/deriving-a-class-from-cobject.md)
