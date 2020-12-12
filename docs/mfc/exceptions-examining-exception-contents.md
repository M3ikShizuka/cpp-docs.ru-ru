---
description: 'Дополнительные сведения об исключениях: анализ содержимого исключений'
title: Исключения. Анализ содержимого исключений
ms.date: 11/04/2016
helpviewer_keywords:
- exception handling [MFC], MFC
- try-catch exception handling [MFC], MFC function exceptions
- catch blocks, MFC function exceptions
- CException class [MFC], class exceptions
- try-catch exception handling [MFC], exception contents
- throwing exceptions [MFC], exception contents
ms.assetid: dfda4782-b969-4f60-b867-cc204ea7f33a
ms.openlocfilehash: aef28d79bd6cad1d810700015930b14b5fdedddc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97290626"
---
# <a name="exceptions-examining-exception-contents"></a>Исключения. Анализ содержимого исключений

Хотя **`catch`** аргумент блока может быть практически любого типа данных, функции MFC создают исключения типов, производных от класса `CException` . Чтобы перехватить исключение, вызванное функцией MFC, необходимо написать блок, **`catch`** аргумент которого является указателем на `CException` объект (или объект, производный от `CException` , например `CMemoryException` ). В зависимости от конкретного типа исключения можно изучить элементы данных объекта исключения, чтобы собрать сведения о конкретной причине исключения.

Например, `CFileException` тип имеет `m_cause` элемент Data, который содержит перечислимый тип, указывающий причину исключения файла. Примеры возможных возвращаемых значений: `CFileException::fileNotFound` и `CFileException::readOnly` .

В следующем примере показано, как проверить содержимое объекта `CFileException` . Другие типы исключений можно проверить аналогичным образом.

[!code-cpp[NVC_MFCExceptions#13](codesnippet/cpp/exceptions-examining-exception-contents_1.cpp)]

Дополнительные сведения см. [в разделе исключения: освобождение объектов в исключениях](exceptions-freeing-objects-in-exceptions.md) и [исключениях: перехват и удаление исключений](exceptions-catching-and-deleting-exceptions.md).

## <a name="see-also"></a>См. также раздел

[Обработка исключений](exception-handling-in-mfc.md)
