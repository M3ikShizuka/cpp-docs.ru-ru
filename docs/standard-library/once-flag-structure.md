---
description: 'Дополнительные сведения: структура once_flag'
title: Структура once_flag
ms.date: 09/17/2018
f1_keywords:
- mutex/std::once_flag
ms.assetid: 71bfb88d-ca8c-4082-a6e1-ff52151e8629
ms.openlocfilehash: 4419353e68da5929d8abed9b2c718438855057e0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97338000"
---
# <a name="once_flag-structure"></a>Структура once_flag

Представляет объект **`struct`** , используемый с функцией шаблона [call_once](../standard-library/mutex-functions.md#call_once) , чтобы код инициализации вызывался только один раз, даже при наличии нескольких потоков выполнения.

## <a name="syntax"></a>Синтаксис

Структура once_flag {constexpr once_flag () не except;};

## <a name="remarks"></a>Комментарии

`once_flag` **`struct`** Имеет только конструктор по умолчанию.

Объекты типа `once_flag` могут быть созданы, но их нельзя скопировать.

## <a name="requirements"></a>Требования

**Заголовок:**\<mutex>

**Пространство имен:** std

## <a name="see-also"></a>См. также раздел

[Справочник по файлам заголовков](../standard-library/cpp-standard-library-header-files.md)\
[\<mutex>](../standard-library/mutex.md)
