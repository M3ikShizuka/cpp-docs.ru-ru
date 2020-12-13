---
description: 'Дополнительные сведения: no_namespace атрибута импорта'
title: no_namespace атрибут импорта
ms.date: 08/29/2019
f1_keywords:
- no_namespace
helpviewer_keywords:
- no_namespace attribute
ms.assetid: 5d81b741-a558-451b-b493-1f3b18967337
ms.openlocfilehash: e1503015f455af65a138e4e3e6843fd0516d2773
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97333319"
---
# <a name="no_namespace-import-attribute"></a>no_namespace атрибут импорта

**Блок, относящийся только к языку C++**

Указывает, что компилятор не создает имя пространства имен.

## <a name="syntax"></a>Синтаксис

> **no_namespace** типов **#import** *-Library*

## <a name="remarks"></a>Комментарии

Содержимое библиотеки типов в файле заголовка `#import` обычно определяется в пространстве имен. Имя пространства имен указывается в `library` инструкции ИСХОДНОГО IDL-файла. Если указан атрибут **no_namespace** , компилятор не создает это пространство имен.

Если вы хотите использовать другое имя пространства имен, используйте вместо него атрибут [rename_namespace](../preprocessor/rename-namespace.md) .

**Завершение блока, относящегося только к языку C++**

## <a name="see-also"></a>См. также раздел

[атрибуты #import](../preprocessor/hash-import-attributes-cpp.md)\
[#import - директива](../preprocessor/hash-import-directive-cpp.md)
