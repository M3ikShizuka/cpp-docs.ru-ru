---
description: Дополнительные сведения см. в статье поддержка COM+ 1,0 в проектах ATL.
title: Поддержка COM+ 1,0 в проектах ATL
ms.date: 11/04/2016
f1_keywords:
- vc.appwiz.ATL.MTS
helpviewer_keywords:
- ATL projects, COM+ 1.0 support
ms.assetid: 51fb08ac-d632-4657-a4e0-d3f989f0b6f8
ms.openlocfilehash: 8e196bccf25667da28532248765e47906fdcee97
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97141288"
---
# <a name="com-10-support-in-atl-projects"></a>Поддержка COM+ 1,0 в проектах ATL

С помощью [мастера проектов ATL](../../atl/reference/creating-an-atl-project.md) можно создать проект с базовой поддержкой компонентов COM+ 1,0.

COM+ 1,0 предназначен для разработки распределенных приложений на основе компонентов. Она также предоставляет инфраструктуру времени выполнения для развертывания этих приложений и управления ими.

Если установлен флажок **Поддержка COM+ 1,0** , мастер изменяет скрипт сборки на шаге компоновки. В частности, проект COM+ 1,0 связан со следующими библиотеками:

- комсвкс. lib

- Мтксгуид. lib

Если установлен флажок **Поддержка COM+ 1,0** , можно также выбрать пункт **Поддержка Регистратор компонентов**. Регистратор компонентов позволяет объекту COM+ 1,0 получать список компонентов, регистрировать компоненты или отменять регистрацию компонентов (по отдельности или все одновременно).

## <a name="see-also"></a>См. также раздел

[Основы COM-объектов ATL](../../atl/fundamentals-of-atl-com-objects.md)<br/>
[Программирование с помощью ATL и кода Run-Time C](../../atl/programming-with-atl-and-c-run-time-code.md)<br/>
[Конфигурации проектов ATL по умолчанию](../../atl/reference/default-atl-project-configurations.md)
