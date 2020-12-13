---
description: 'Дополнительные сведения: Ошибка компилятора ресурсов ресурсов RC2144'
title: Ошибка компилятора ресурсов RC2144
ms.date: 11/04/2016
f1_keywords:
- RC2144
helpviewer_keywords:
- RC2144
ms.assetid: 1b3ff39a-92cd-4a04-b1a3-b1fa6a805813
ms.openlocfilehash: 8b40f989e4319b16a9a983f5e4e377aeb357e8f7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97133514"
---
# <a name="resource-compiler-error-rc2144"></a>Ошибка компилятора ресурсов RC2144

PRIMARY LANGUAGE ID не является числом

PRIMARY LANGUAGE ID должен быть шестнадцатеричным идентификатором языка. Допустимые идентификаторы языков см. в разделе [Языки и настройки для стран и регионов](../../c-runtime-library/locale-names-languages-and-country-region-strings.md) в *справочнике по библиотеке среды выполнения* .

Эта ошибка также может возникнуть, если с помощью какого-либо средства ресурсы были добавлены в RC-файл или удалены из RC-файла. Чтобы устранить эту проблему, откройте RC-файл в текстовом редакторе и вручную удалите все неиспользуемые ресурсы.
