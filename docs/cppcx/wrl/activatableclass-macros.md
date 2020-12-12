---
description: 'Дополнительные сведения о: Активатаблекласс Macros'
title: Макрос ActivatableClass
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- ActivatableClass
- ActivatableClassWithFactory
- ActivatableClassWithFactoryEx
helpviewer_keywords:
- ActivatableClassWithFactory
- ActivatableClass
- ActivatableClassWithFactoryEx
ms.assetid: 9bd64709-ec2c-4678-8c96-ea5982622bdd
ms.openlocfilehash: 2b59101373de72ca88338750bb7fe9169376ac65
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97287948"
---
# <a name="activatableclass-macros"></a>Макрос ActivatableClass

Заполняет внутренний кэш, содержащий фабрику, которая может создать экземпляр указанного класса.

## <a name="syntax"></a>Синтаксис

```cpp
ActivatableClass(
   className
);

ActivatableClassWithFactory(
   className,
   factory
);

ActivatableClassWithFactoryEx(
   className,
   factory,
   serverName
);
```

### <a name="parameters"></a>Параметры

*className*<br/>
Имя создаваемого класса.

*фабрика*<br/>
Фабрика, которая создаст экземпляр указанного класса.

*serverName*<br/>
Имя, указывающее подмножество фабрик в модуле.

## <a name="remarks"></a>Комментарии

Не используйте эти макросы с классической моделью COM, если не используется `#undef` директива, чтобы гарантировать `__WRL_WINRT_STRICT__` Удаление определения макроса.

## <a name="requirements"></a>Требования

**Заголовок:** Module. h

**Пространство имен:** Microsoft::WRL

## <a name="see-also"></a>См. также раздел

[Класс Module](module-class.md)
