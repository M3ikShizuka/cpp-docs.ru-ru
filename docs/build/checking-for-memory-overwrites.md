---
description: 'Подробнее о следующем: Проверка затирания памяти'
title: Проверка затирания памяти
ms.date: 11/04/2016
helpviewer_keywords:
- memory, overwrites
ms.assetid: da7c5d77-a267-415f-a8ab-ee5ce5bfc286
ms.openlocfilehash: 53361a6aea3de54017be3c966f9500accd21ced1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97163175"
---
# <a name="checking-for-memory-overwrites"></a>Проверка затирания памяти

Если при вызове функции управления кучей вы получаете ошибку, связанную с нарушением прав доступа, возможно, ваша программа вызвала повреждение кучи. Как правило, в такой ситуации проявляются следующие признаки:

```
Access Violation in _searchseg
```

Функция [_heapchk](../c-runtime-library/reference/heapchk.md) доступна в сборках отладки и выпуска (только для Windows NT) для проверки целостности кучи библиотеки времени выполнения. Вы можете использовать `_heapchk` аналогично функции `AfxCheckMemory` для изоляции перезаписи кучи, например:

```
if(_heapchk()!=_HEAPOK)
   DebugBreak();
```

Если эта функция завершается сбоем, необходимо изолировать точку, в которой произошло повреждение кучи.

## <a name="see-also"></a>См. также

[Устранение проблем сборки выпуска](fixing-release-build-problems.md)
