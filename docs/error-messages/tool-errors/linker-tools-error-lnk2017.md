---
description: 'Дополнительные сведения: Ошибка средств компоновщика LNK2017'
title: Ошибка средств компоновщика LNK2017
ms.date: 11/04/2016
f1_keywords:
- LNK2017
helpviewer_keywords:
- LNK2017
ms.assetid: f7c21733-b0fb-4888-a295-9b453ba6ee77
ms.openlocfilehash: e4215d7c1730f85f43c2440163fa03ad97c741e5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338444"
---
# <a name="linker-tools-error-lnk2017"></a>Ошибка средств компоновщика LNK2017

перемещение символа в "сегмент" недопустимо без/LARGEADDRESSAWARE: нет

Вы пытаетесь создать 64-разрядный образ с 32-битным адресом. Для этого необходимо выполнить следующие действия.

- Используйте фиксированный адрес загрузки.

- Ограничьте образ до 3 ГБ.

- Укажите [/LARGEADDRESSAWARE: No](../../build/reference/largeaddressaware-handle-large-addresses.md).
