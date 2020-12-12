---
description: 'Дополнительные сведения: NULL и неопределенные макросы'
title: Пустой и неопределенный макрос
ms.date: 11/04/2016
helpviewer_keywords:
- NMAKE program, undefined macros
- Null macros in NMAKE
- macros, null and undefined
- undefined macros and NMAKE
- NMAKE program, null macros
ms.assetid: 1db4611a-1755-4328-b00f-d35365af8b6c
ms.openlocfilehash: 639afda727f1ebb1f4d7d602ed7cf01d6c914a33
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97209728"
---
# <a name="null-and-undefined-macros"></a>Пустой и неопределенный макрос

И NULL, и неопределенные макросы разворачиваются до значений NULL, но макрос, определенный как строка NULL, считается определенным в выражениях предварительной обработки. Чтобы определить макрос как пустую строку, не указывайте символы, кроме пробелов или знаков табуляции после знака равенства (=) в командной строке или командном файле, и заключите строку или определение в двойные кавычки (""). Чтобы отменить определение макроса, используйте **! UNDEF.** Дополнительные сведения см. в статье о [директивах предварительной обработки файлов Makefile](makefile-preprocessing-directives.md).

## <a name="see-also"></a>См. также раздел

[Определение макроса NMAKE](defining-an-nmake-macro.md)
