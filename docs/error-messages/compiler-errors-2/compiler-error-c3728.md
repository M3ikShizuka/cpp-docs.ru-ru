---
description: 'Дополнительные сведения о: Ошибка компилятора C3728'
title: Ошибка компилятора C3728
ms.date: 11/04/2016
f1_keywords:
- C3728
helpviewer_keywords:
- C3728
ms.assetid: 6b510cb1-887f-4fcd-9a1f-3bb720417ed1
ms.openlocfilehash: 0cfcbd38928a153e3f5a58c1ec66b7e1c5bfd08d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97245100"
---
# <a name="compiler-error-c3728"></a>Ошибка компилятора C3728

"событие": событие не имеет метода Raise

Метаданные, созданные с помощью языка, например C#, которые не позволяют вызывать событие извне класса, в котором он был определен, были добавлены с помощью директивы [#using](../../preprocessor/hash-using-directive-cpp.md) , а Visual C++ программы, использующей программирование CLR, попытались вызвать событие.

Чтобы создать событие в программе, разработанной на языке, таком как C#, класс, содержащий событие, должен также определять открытый метод, который вызывает событие.
