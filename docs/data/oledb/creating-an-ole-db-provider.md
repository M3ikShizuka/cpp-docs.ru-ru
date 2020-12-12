---
description: 'Дополнительные сведения: создание поставщика OLE DB'
title: Создание поставщика OLE DB
ms.date: 10/13/2018
helpviewer_keywords:
- OLE DB providers, creating
- OLE DB provider templates, creating providers
ms.assetid: f73017c3-c89f-41a6-a306-ea992cf6092c
ms.openlocfilehash: 69dc9311a79f2739636633b2d268343a92d2dac9
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97287805"
---
# <a name="creating-an-ole-db-provider"></a>Создание поставщика OLE DB

Для создания поставщика OLE DB рекомендуется использовать мастера для создания проекта ATL COM и поставщика, а затем изменить файлы с помощью шаблонов OLE DB. При настройке поставщика можно закомментировать ненужные свойства и добавить дополнительные интерфейсы.

Основными шагами являются следующие:

1. **Мастер проектов ATL** используется для создания основных файлов проекта и **мастера поставщика ATL OLEDB** для создания поставщика (выберите **поставщик OLEDB ATL** из папки **установленные**  >  **Visual C++**  >  **ATL** в **меню Добавить новый элемент**).

   > [!NOTE]
   > Проект должен включать поддержку MFC перед добавлением **поставщика OLEDB ATL**.

1. Измените код в `Execute` методе в [Ккустомровсет (кустомрс. h)](cmyproviderrowset-myproviderrs-h.md). Пример см. в разделе [считывание строк в поставщик OLE DB](../../data/oledb/reading-strings-into-the-ole-db-provider.md).

1. Измените сопоставления свойств в [кустомдс. h](cmyprovidersource-myproviderds-h.md), [кустомсесс. h](cmyprovidersession-myprovidersess-h.md)и [кустомрс. h](cmyproviderrowset-myproviderrs-h.md). Мастер создает сопоставления свойств, которые содержат все свойства, которые может реализовать поставщик. Пройдите по картам свойств и удалите или закомментируйте свойства, которые не требуется поддерживать поставщику.

1. Обновите PROVIDER_COLUMN_MAP, который можно найти в [ккустомровсет (кустомрс. h)](cmyproviderrowset-myproviderrs-h.md). Пример см. в разделе [Хранение строк в поставщике OLE DB](../../data/oledb/storing-strings-in-the-ole-db-provider.md).

1. Когда вы будете готовы протестировать поставщик, его можно протестировать, пытаясь найти поставщика в перечислении поставщика. Примеры кода теста, который находит поставщик в перечислении, см. в статьях примеры [catdb](https://github.com/Microsoft/VCSamples/tree/master/VC2008Samples/ATL/OLEDB/Consumer/catdb) и [Дбвиевер](https://github.com/Microsoft/VCSamples/tree/master/VC2008Samples/ATL/OLEDB/Consumer/dbviewer) или пример [реализации простого потребителя](../../data/oledb/implementing-a-simple-consumer.md).

1. Добавьте необходимые дополнительные интерфейсы. Пример см. в разделе [улучшение простого поставщика Read-Only](../../data/oledb/enhancing-the-simple-read-only-provider.md).

   > [!NOTE]
   > По умолчанию мастера создают код, который соответствует требованиям OLE DB уровня 0. Чтобы убедиться, что приложение остается соответствующим уровню 0, не удаляйте из кода ни один из созданных мастером интерфейсов.

## <a name="see-also"></a>См. также раздел

[Пример CatDB: Обозреватель схемы источника данных](https://github.com/Microsoft/VCSamples/tree/master/VC2008Samples/ATL/OLEDB/Consumer/catdb)<br/>
[Пример Дбвиевер: Обозреватель баз данных](https://github.com/Microsoft/VCSamples/tree/master/VC2008Samples/ATL/OLEDB/Consumer/dbviewer)
