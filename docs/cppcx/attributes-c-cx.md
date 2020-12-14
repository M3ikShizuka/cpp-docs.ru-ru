---
description: 'Дополнительные сведения: атрибуты (C++/CX)'
title: Атрибуты (C++/CX)
ms.date: 12/30/2016
ms.assetid: 4438e03c-4de3-433d-abcc-31aa863bc0e0
ms.openlocfilehash: 82299db6b5c11521584b8dd400b401ec0df78c72
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97302781"
---
# <a name="attributes-ccx"></a>Атрибуты (C++/CX)

Атрибут — это специальный тип ссылочного класса, который можно добавить в квадратные скобки, чтобы среда выполнения Windows типы и методы для указания определенных поведений при создании метаданных. Несколько предварительно определенных атрибутов, например  [Windows:: Foundation:: Metadata:: WebHostHidden](/uwp/api/windows.foundation.metadata.webhosthiddenattribute), обычно используются в коде C++/CX. В этом примере показано, как атрибут применяется к классу.

[!code-cpp[cx_attributes#01](../cppcx/codesnippet/CPP/cx_attributes/class1.h#01)]

## <a name="custom-attributes"></a>Настраиваемые атрибуты

Также можно определять настраиваемые атрибуты. Настраиваемые атрибуты должны соответствовать следующим правилам среда выполнения Windows:

- настраиваемые атрибуты могут содержать только открытые поля;

- поля настраиваемого атрибута можно инициализировать при применении атрибута к классу;

- поле может относиться к одному из следующих типов:

  - int32 (int)

  - uint32 (unsigned int)

  - bool

  - Platform::String^

  - Windows::Foundation::HResult

  - Platform::Type^

  - public enum class (включая перечисления, определяемые пользователем).

В следующем примере показано, как определить настраиваемый атрибут, а затем инициализировать его при использовании.

[!code-cpp[cx_attributes#02](../cppcx/codesnippet/CPP/cx_attributes/class1.h#02)]

## <a name="see-also"></a>См. также раздел

[Система типов (C++/CX)](../cppcx/type-system-c-cx.md)<br/>
[Справочник по языку C++/CX](../cppcx/visual-c-language-reference-c-cx.md)<br/>
[Справочник по пространствам имен](../cppcx/namespaces-reference-c-cx.md)
