---
description: 'Дополнительные сведения: Отладка поставщика'
title: Отладка поставщика
ms.date: 10/29/2018
helpviewer_keywords:
- debugging [C++], providers
- OLE DB providers, debugging
- Visual C++ debugger, debugging providers
- Visual C++ debugger
ms.assetid: 90d4e7db-06ea-4de0-a7f4-4f3751d50d93
ms.openlocfilehash: 9a178bfa55f8efeb11a3265ab8aa14a5418d7516
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97287584"
---
# <a name="debugging-your-provider"></a>Отладка поставщика

Существует два способа отладки поставщика:

- Так как поставщики создаются в процессе, можно создать некоторый код потребителя, используя шаблоны OLE DB потребителей, и в обычном режиме перейти к поставщику.

- Вы можете использовать различные служебные программы, которые входят в состав Visual C++.

## <a name="to-use-debugging"></a>Использование отладки

1. Откройте проект поставщика.

1. В меню **проекты** выберите пункт **свойства**.

1. В диалоговом окне **страницы свойств** перейдите на вкладку **Отладка** .

1. Выберите необходимые параметры, нажмите кнопку **ОК**.

1. Задайте точки останова, а затем выполните отладку обычным образом.

## <a name="see-also"></a>См. также раздел

[Работа с шаблонами поставщика OLE DB](../../data/oledb/working-with-ole-db-provider-templates.md)
