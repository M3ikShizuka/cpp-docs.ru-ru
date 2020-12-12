---
description: 'Дополнительные сведения: inject_statement атрибута импорта'
title: inject_statement атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- inject_statement
helpviewer_keywords:
- inject_statement attribute
ms.assetid: 07d6f0f4-d9fb-4e18-aa62-f235f142ff5e
ms.openlocfilehash: b7ab8059e95ed3799857fe1b899ef2efff729ffb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97236429"
---
# <a name="inject_statement-import-attribute"></a>inject_statement атрибут импорта

**Блок, относящийся только к языку C++**

Вставляет свой аргумент как исходный текст в заголовок библиотеки типов.

## <a name="syntax"></a>Синтаксис

> inject_statement типа **#import** *-Library* **(** "*Исходный текст*" **)**

### <a name="parameters"></a>Параметры

*исходный текст*\
Исходный текст, вставляемый в файл заголовка библиотеки типов.

## <a name="remarks"></a>Комментарии

Текст помещается в начало объявления пространства имен, которое служит оболочкой для содержимого *библиотеки типов* в файле заголовка.

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
