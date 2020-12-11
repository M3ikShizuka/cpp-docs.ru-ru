---
description: 'Дополнительные сведения: ошибка средства оценки выражений CXX0033'
title: Ошибка вычислителя выражений CXX0033
ms.date: 11/04/2016
f1_keywords:
- CXX0033
helpviewer_keywords:
- CAN0033
- CXX0033
ms.assetid: 0bd62c5b-de89-481f-9b12-88fe84805afe
ms.openlocfilehash: 714499d8d1bc0812395576fe27be690997982065
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97160328"
---
# <a name="expression-evaluator-error-cxx0033"></a>Ошибка вычислителя выражений CXX0033

Ошибка в сведениях о типе OMF

Исполняемый файл не имеет допустимого формата объекта (OMF) для отладки.

Эта ошибка идентична CAN0033.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>Чтобы устранить ошибку, проверьте указанные ниже возможные причины ее возникновения.

1. Исполняемый файл не был создан компоновщиком, выпущенным в данной версии Visual C++. Повторно свяжите объектный код с использованием текущей версии LINK.exe.

1. Возможно, файл exe поврежден. Перекомпилируйте и повторно свяжите программу.
