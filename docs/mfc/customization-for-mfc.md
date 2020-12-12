---
description: Дополнительные сведения о настройке MFC
title: Настройка для MFC
ms.date: 11/04/2016
helpviewer_keywords:
- customizations, MFC Extensions
ms.assetid: 3b1b7532-8cc9-48dc-9bbe-7fd4060530b5
ms.openlocfilehash: 50df32d4743381e1212eae53b695e2355bc8d0e1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97309411"
---
# <a name="customization-for-mfc"></a>Настройка для MFC

В этом разделе приводятся советы по настройке приложения MFC.

## <a name="general-customizations"></a>Общие настройки

Вы можете сохранить и загрузить состояние приложения в реестр. При включении этого параметра приложение будет загружать свое начальное состояние из реестра. При изменении первоначального макета закрепления для приложения необходимо очистить данные реестра для приложения. В противном случае данные в реестре будут переопределять все изменения, внесенные в первоначальный макет.

## <a name="class-specific-customizations"></a>Настройки Class-Specific

Дополнительные советы по настройке можно найти в следующих разделах:

- [Класс CBasePane](reference/cbasepane-class.md)

- [Класс CDockablePane](reference/cdockablepane-class.md)

- [Класс Кдоккингманажер](reference/cdockingmanager-class.md)

- [Класс CMFCBaseTabCtrl](reference/cmfcbasetabctrl-class.md)

## <a name="additional-customization-tips"></a>Дополнительные советы по настройке

[Настройка клавиатуры и мыши](keyboard-and-mouse-customization.md)

[Пользовательские средства](user-defined-tools.md)

## <a name="see-also"></a>См. также раздел

[Классические приложения MFC](mfc-desktop-applications.md)<br/>
[Влияние настройки на безопасность](security-implications-of-customization.md)
