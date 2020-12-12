---
description: 'Дополнительные сведения: сериализация (C++/CLI)'
title: Сериализация (C++/CLI)
ms.date: 11/04/2016
helpviewer_keywords:
- serialization [C++]
- SerializableAttribute class, managed applications
- NonSerializedAttribute class, managed applications
- managed code [C++], serializing
- .NET Framework [C++], serialization
- serialization [C++], about serialization
ms.assetid: 869010ca-74e1-4989-b409-4643cdb94084
ms.openlocfilehash: 1524ed5d4a000d2006f6f830b1d82119d170c3b2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97164605"
---
# <a name="serialization-ccli"></a>Сериализация (C++/CLI)

Сериализация (процесс хранения состояния объекта или элемента на постоянный носитель) управляемых классов (включая отдельные поля или свойства) поддерживается <xref:System.SerializableAttribute> <xref:System.NonSerializedAttribute> классами и.

## <a name="remarks"></a>Комментарии

Примените настраиваемый атрибут **SerializableAttribute** к управляемому классу, чтобы сериализовать весь класс или применить его только к конкретным полям или свойствам для сериализации частей управляемого класса. Используйте настраиваемый атрибут **NonSerializedAttribute** , чтобы исключить из сериализации поля или свойства управляемого класса.

## <a name="example"></a>Пример

### <a name="description"></a>Описание

В следующем примере класс `MyClass` (и свойство `m_nCount` ) помечаются как сериализуемый. Однако `m_nData` свойство не сериализуется, как указано **несериализованным** пользовательским атрибутом:

### <a name="code"></a>Код

```cpp
// serialization_and_mcpp.cpp
// compile with: /LD /clr
using namespace System;

[ Serializable ]
public ref class MyClass {
public:
   int m_nCount;
private:
   [ NonSerialized ]
   int m_nData;
};
```

### <a name="comments"></a>Комментарии

Обратите внимание, что к обоим атрибутам можно обращаться с помощью «краткого имени» (**сериализуемых** и **несериализуемых**). Это Подробнее объясняется в разделах [применение атрибутов](/dotnet/standard/attributes/applying-attributes).

## <a name="see-also"></a>См. также раздел

[Программирование .NET с использованием C++/CLI (Visual C++)](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)
