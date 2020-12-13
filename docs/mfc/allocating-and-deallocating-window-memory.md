---
description: 'Дополнительные сведения: выделение и освобождение памяти окна'
title: Выделение и освобождение памяти окна
ms.date: 11/04/2016
helpviewer_keywords:
- memory allocation, window objects
- memory deallocation
- storage for window objects [MFC]
- memory deallocation, window memory
- window objects [MFC], deallocating memory for
- storage for window objects [MFC], allocating
ms.assetid: 7c962539-8461-4846-b5ca-fe3b15c313dc
ms.openlocfilehash: 7648914289babffdfb5195f1ec53cd736e26892c
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97343722"
---
# <a name="allocating-and-deallocating-window-memory"></a>Выделение и освобождение памяти окна

Не используйте **`delete`** оператор C++ для уничтожения окна или представления фрейма. Вместо этого вызовите `CWnd` функцию члена `DestroyWindow` . Таким образом, окна фрейма должны выделяться в куче с оператором **`new`** . Будьте внимательны при выделении окон фрейма в кадре стека или глобально. Другие окна должны выделяться в кадре стека везде, где это возможно.

## <a name="what-do-you-want-to-know-more-about"></a>Что вы хотите узнать подробнее

- [Создание окон](creating-windows.md)

- [Последовательность уничтожения окна](window-destruction-sequence.md)

- [Отсоединение CWnd от HWND](detaching-a-cwnd-from-its-hwnd.md)

## <a name="see-also"></a>См. также раздел

[Уничтожение объектов Window](destroying-window-objects.md)
