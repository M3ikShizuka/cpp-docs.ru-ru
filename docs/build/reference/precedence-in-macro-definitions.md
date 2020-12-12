---
description: 'Дополнительные сведения: приоритет в определениях макросов'
title: Приоритет в макроопределениях
ms.date: 11/04/2016
helpviewer_keywords:
- NMAKE program, precedence in macro definitions
- macros, precedence
ms.assetid: 0c13182d-83cb-4cbd-af2d-f4c916b62aeb
ms.openlocfilehash: 1738c4ba77f330103395278a6daae169b04fae4c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97225899"
---
# <a name="precedence-in-macro-definitions"></a>Приоритет в макроопределениях

Если макрос имеет несколько определений, NMAKE использует определение с наивысшим приоритетом. В следующем списке показан порядок приоритета, от самого высокого до самого низкого:

1. Макрос, определенный в командной строке

1. Макрос, определенный в файле makefile или include

1. Наследуемый макрос переменной среды

1. Макрос, определенный в файле Tools.ini

1. Предопределенный макрос, например [CC](command-macros-and-options-macros.md) и [as](command-macros-and-options-macros.md) .

Используйте параметр/E, чтобы макросы, унаследованные от переменных среды, переопределяли макросы makefile с тем же именем. Используйте **! UNDEF** для переопределения командной строки.

## <a name="see-also"></a>См. также раздел

[Определение макроса NMAKE](defining-an-nmake-macro.md)
