---
description: 'Подробнее о: ExitInstance функция члена'
title: Функция-член ExitInstance
ms.date: 11/04/2016
f1_keywords: []
helpviewer_keywords:
- programs [MFC], terminating
- CWinApp class [MFC], ExitInstance
- ExitInstance method [MFC]
ms.assetid: 5bb597bd-8dab-4d49-8bcf-9c45aa8be4a2
ms.openlocfilehash: a469d29c6b8dc2b822928293ee3bd083ccce95e7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97314728"
---
# <a name="exitinstance-member-function"></a>Функция-член ExitInstance

Функция-член [ExitInstance](reference/cwinapp-class.md#exitinstance) класса [CWinApp](reference/cwinapp-class.md) вызывается каждый раз при завершении копии приложения, обычно в результате того, как пользователь закрывает приложение.

Переопределите `ExitInstance` , если требуется специальная обработка очистки, например освобождение ресурсов интерфейса графических устройств (GDI) или освобождение памяти, используемой во время выполнения программы. Однако очистка стандартных элементов, таких как документы и представления, обеспечивается платформой с другими переопределяемыми функциями для выполнения специальной очистки, характерной для этих объектов.

## <a name="see-also"></a>См. также раздел

[CWinApp: класс Application](cwinapp-the-application-class.md)
