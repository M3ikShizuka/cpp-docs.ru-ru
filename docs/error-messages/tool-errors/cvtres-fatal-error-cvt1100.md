---
description: 'Дополнительные сведения: Неустранимая ошибка CVTRES CVT1100'
title: Неустранимая ошибка CVTRES CVT1100
ms.date: 11/04/2016
f1_keywords:
- CVT1100
helpviewer_keywords:
- CVT1100
ms.assetid: 886e88dd-5818-4b5f-84f2-d2a3d75f0aaf
ms.openlocfilehash: e54a3aeaf8b0b7955ab7e9cb7558c97a57fc95e0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97119740"
---
# <a name="cvtres-fatal-error-cvt1100"></a>Неустранимая ошибка CVTRES CVT1100

дублирующий ресурс — тип: тип, имя: имя, язык: язык, флаги: флаги, размер: размер

Указанный ресурс был указан несколько раз.

Эту ошибку можно получить, если компоновщик создает библиотеку типов и вы не указали [/TLBID](../../build/reference/tlbid-specify-resource-id-for-typelib.md) , а ресурс в проекте уже использует 1. В этом случае укажите/TLBID и укажите другое число до 65535.
