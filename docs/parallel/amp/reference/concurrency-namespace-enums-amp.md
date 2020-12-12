---
description: 'Дополнительные сведения о: перечисление пространств имен Concurrency (AMP)'
title: Перечисления пространства имен Concurrency (AMP)
ms.date: 11/04/2016
f1_keywords:
- amp/Concurrency::access_type
- amp/Concurrency::queuing_mode
ms.assetid: 4c87457e-184f-4992-81ab-ca75e7d524ab
ms.openlocfilehash: 60f4b325de47a600ee5a28f30ecc4a06fc2082a2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97284906"
---
# <a name="concurrency-namespace-enums-amp"></a>Перечисления пространства имен Concurrency (AMP)

[Перечисление access_type](#access_type)\
[Перечисление queuing_mode](#queuing_mode)

## <a name="access_type-enumeration"></a><a name="access_type"></a> Перечисление access_type

Тип перечисления, используемый для обозначения различных типов доступа к данным.

```cpp
enum access_type;
```

### <a name="values"></a>Значения

|Имя|Описание|
|----------|-----------------|
|`access_type_auto`|Автоматически выберите оптимальное значение `access_type` для ускорителя.|
|`access_type_none`|Специальное. Выделение доступно только в ускорителе, а не на ЦП.|
|`access_type_read`|Используемый. Выделение доступно для ускорителя и доступно для чтения на ЦП.|
|`access_type_read_write`|Используемый. Выделение доступно для ускорителя и доступно для записи в ЦП.|
|`access_type_write`|Используемый. Выделение доступно для ускорителя и доступно для чтения и записи в ЦП.|

## <a name="queuing_mode-enumeration"></a><a name="queuing_mode"></a> Перечисление queuing_mode

Указывает режимы работы в очереди, которые поддерживаются ускорителем.

```cpp
enum queuing_mode;
```

### <a name="values"></a>Значения

|Имя|Описание|
|----------|-----------------|
|`queuing_mode_immediate`|Режим очереди, указывающий, что любые команды, например [Parallel_for_each функции (C++ amp)](concurrency-namespace-functions-amp.md#parallel_for_each), отправляются соответствующему устройству ускорителя, как только они возвращаются вызывающему.|
|`queuing_mode_automatic`|Режим очереди, указывающий, что команды ставятся в очередь в очереди команд, соответствующей объекту [accelerator_view](accelerator-view-class.md) . Команды отправляются на устройство при вызове [accelerator_view:: Flush](accelerator-view-class.md#flush) .|

## <a name="see-also"></a>См. также раздел

[Пространство имен Concurrency (C++ AMP)](concurrency-namespace-cpp-amp.md)
