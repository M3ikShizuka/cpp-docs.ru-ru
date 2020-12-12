---
description: 'Дополнительные сведения о пространстве имен Platform:: Metadata.'
title: Пространство имен Platform::Metadata
ms.date: 12/30/2016
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::Metadata
helpviewer_keywords:
- Platform::Metadata Namespace
ms.assetid: e3e114d8-a4b0-47f0-865a-9ce9d7212e86
ms.openlocfilehash: 5dd699c0136c4ee37462dd22f9ee27bec345e8b5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97308397"
---
# <a name="platformmetadata-namespace"></a>Пространство имен Platform::Metadata

Это пространство имен содержит атрибуты, которые изменяют объявления типов.

## <a name="syntax"></a>Синтаксис

```cpp
namespace Platform {
   namespace Metadata {
}}
```

### <a name="members"></a>Члены

Хотя это пространство имен предназначено для внутреннего использования, следующие его члены могут отображаться в браузерах.

|Имя|Комментарий|
|----------|------------|
|Атрибут|Базовый класс для атрибутов.|
|[Platform:: Metadata::D атрибут Ефаултмембераттрибуте](../cppcx/platform-metadata-defaultmemberattribute-attribute.md)|Указывает предпочтительную вызываемую функцию из нескольких возможных перегруженных функций.|
|[Атрибут Platform::Metadata::FlagsAttribute](../cppcx/platform-metadata-flagsattribute-attribute.md)|Объявляет перечисление как перечисление битовых полей.<br /><br /> В следующем примере показано применение атрибута `Flags` к перечислению.<br /><br /> `[Flags] enum class MyEnumeration { enumA = 1, enumB = 2, enumC = 3}`|
|[Platform::Metadata::RuntimeClassNameAttribute](../cppcx/platform-metadata-runtimeclassname.md)|Проверяет, что закрытому классу ссылки присвоено допустимое имя класса среды выполнения.|

## <a name="inheritance-hierarchy"></a>Иерархия наследования

`Platform`

### <a name="requirements"></a>Требования

**Метаданные:** Platform. winmd

**Пространство имен:** Platform::Metadata

## <a name="see-also"></a>См. также раздел

[Пространство имен платформы](platform-namespace-c-cx.md)
