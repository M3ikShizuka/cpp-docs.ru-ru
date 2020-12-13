---
description: 'Дополнительные сведения: глобальные функции COM компилятора'
title: Глобальные функции COM-модели компилятора
ms.date: 11/04/2016
helpviewer_keywords:
- cl.exe compiler, COM support
- COM, compiler support
ms.assetid: 74449d26-50a2-47c7-b175-7cf2cf83533e
ms.openlocfilehash: d678372bdc5703aa05fdf093b84075b7286c4b9d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335550"
---
# <a name="compiler-com-global-functions"></a>Глобальные функции COM-модели компилятора

**Блок, относящийся только к системам Microsoft**

Доступны следующие процедуры.

|Функция|Описание|
|--------------|-----------------|
|[_com_raise_error](../cpp/com-raise-error.md)|Вызывает исключение [_com_error](../cpp/com-error-class.md) в ответ на сбой.|
|[_set_com_error_handler](../cpp/set-com-error-handler.md)|Заменяет функцию по умолчанию, используемую для обработки ошибок COM.|
|[ConvertBSTRToString](../cpp/convertbstrtostring.md)|Преобразует значение типа `BSTR` в значение типа `char *`.|
|[ConvertStringToBSTR](../cpp/convertstringtobstr.md)|Преобразует значение типа `char *` в значение типа `BSTR`.|

**Завершение блока, относящегося только к системам Майкрософт**

## <a name="see-also"></a>См. также

[Классы поддержки COM компилятора](../cpp/compiler-com-support-classes.md)<br/>
[Поддержка COM компилятором](../cpp/compiler-com-support.md)
