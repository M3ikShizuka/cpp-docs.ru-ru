---
description: 'Дополнительные сведения: BSCMAKE Error BK1513'
title: Ошибка BSCMAKE BK1513
ms.date: 11/04/2016
f1_keywords:
- BK1513
helpviewer_keywords:
- BK1513
ms.assetid: 9ba87c09-8d82-4c80-b0cf-a8de63dcf9da
ms.openlocfilehash: bdf26e3268f98e5ab41ef27bbeaa3734a001671a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97238093"
---
# <a name="bscmake-error-bk1513"></a>Ошибка BSCMAKE BK1513

для неинкрементного обновления требуются все файлы .SBR

BSCMAKE не может создать новый BSC-файл, поскольку один или несколько SBR-файлов обрезаны. Чтобы найти имена усеченных SBR, прочитайте предупреждения [BK4502](../../error-messages/tool-errors/bscmake-warning-bk4502.md) , сопровождающие эту ошибку.

BSCMAKE может обновить BSC-файл обрезанным SBR-файлом, но не сможет собрать новый. BSCMAKE может собрать новый BSC-файл по следующим причинам:

- BSC-файл отсутствует.

- Для BSC-файла указано неверное имя файла.

- BSC-файл поврежден.

Чтобы устранить эту проблему, нужно удалить обрезанные SBR-файлы и перестроить решение либо очистить решение, затем перестроить его. (В интегрированной среде разработки выберите **Сборка**, **Очистить решение**, а затем щелкните **Сборка**, **Перестроить решение**.)
