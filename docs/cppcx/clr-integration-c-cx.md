---
description: 'Дополнительные сведения: интеграция со средой CLR (C++/CX)'
title: Интеграция со средой CLR (C++/CX)
ms.date: 01/22/2017
ms.assetid: 76e213cf-2f3d-4181-b35b-9fd25d5b307c
ms.openlocfilehash: ae335168ee456f0461154ab48e9d92325fdc599b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97190241"
---
# <a name="clr-integration-ccx"></a>Интеграция со средой CLR (C++/CX)

Некоторые типы среда выполнения Windows получают специальную обработку в C++/CX и языки, основанные на общеязыковой среде выполнения (CLR). В этой статье рассматривается сопоставление определенных типов в одном языке с другим языком. Например, среда CLR сопоставляет Windows.Foundation.IVector с System.Collections.IList, Windows.Foundation.IMap с System.Collections.IDictionary и т. д. Аналогичным образом, в C++/CX специально отображаются такие типы карт, как Platform::D делегата и Platform:: String.

## <a name="mapping-the-windows-runtime-to-ccx"></a>Сопоставление среда выполнения Windows с C++/CX

Когда C++/CX считывает файл метаданных Windows (. winmd), компилятор автоматически сопоставляет общие среда выполнения Windows пространства имен и типы с пространствами имен и типами C++/CX. Например, числовой тип среда выполнения Windows `UInt32` автоматически сопоставляется с `default::uint32` .

C++/CX сопоставляет несколько других типов среда выполнения Windows с пространством имен **Platform** . Например, обработчик **Windows:: Foundation** HString, представляющий текстовую строку в Юникоде, доступную только для чтения, сопоставляется с `Platform::String` классом C++/CX. Если операция среда выполнения Windows возвращает ошибку HRESULT, она сопоставляется с C++/CX `Platform::Exception` .

C++/CX также сопоставляет определенные типы в среда выполнения Windows пространствах имен, чтобы расширить функциональные возможности типа. Для этих типов C++/CX предоставляет вспомогательные конструкторы и методы, характерные для C++ и недоступные в стандартном файле. winmd типа.

В следующих списках приведены структуры значений, поддерживающие новые конструкторы и вспомогательные методы. Если ранее вы написали код, использующий списки инициализации структуры, измените его, чтобы применить новые конструкторы.

**Windows:: Foundation**

- Точка

- Rect

- Размер

**Windows:: UI**

- Цвет

**Windows:: UI:: XAML**

- CornerRadius

- Длительность

- GridLength

- Thickness

**Windows::UI::Xaml::Interop**

- TypeName

**Windows:: UI:: XAML:: Media**

- Матрица

**Windows:: UI:: XAML:: Media:: Animation**

- KeyTime

- RepeatBehavior

**Windows::UI::Xaml::Media::Media3D**

- Matrix3D

## <a name="mapping-the-clr-to-ccx"></a>Сопоставление среды CLR с C++/CX

Когда компиляторы Microsoft C++ или C# считывают WINMD-файл, они автоматически сопоставляют определенные типы в файле метаданных с соответствующими типами C++/CX или CLR. Например, в среде CLR \<T> интерфейс IVector сопоставляется с IList \<T> . Но в C++/CX \<T> интерфейс IVector не сопоставлен с другим типом.

Иреференце \<T> в среда выполнения Windows сопоставляется со значением NULL \<T> в .NET.

## <a name="see-also"></a>См. также раздел

[Взаимодействие с другими языками](../cppcx/interoperating-with-other-languages-c-cx.md)
