---
description: 'Дополнительные сведения: Неустранимая ошибка NMAKE NMAKE U1073'
title: Неустранимая ошибка NMAKE U1073
ms.date: 11/04/2016
f1_keywords:
- U1073
helpviewer_keywords:
- U1073
ms.assetid: d46bf2dd-400a-4802-9db2-f832e1c97f02
ms.openlocfilehash: bd622f37720cf5e992a1d82ea97ca1ff50344c0c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97345450"
---
# <a name="nmake-fatal-error-u1073"></a>Неустранимая ошибка NMAKE U1073

неизвестно, как сделать "TargetName"

Указанный целевой объект не существует, и нет команды для выполнения или правила вывода.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>Возможные способы устранения этой ошибки

1. Проверьте правильность написания имени целевого объекта.

1. Если *TargetName* является псеудотаржет, укажите его в качестве целевого объекта в другом блоке описания.

1. Если *TargetName* является вызовом макроса, убедитесь, что он не разворачивается в пустую строку.
