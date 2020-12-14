---
description: 'Дополнительные сведения о: Кусерексцептион Class'
title: Класс Кусерексцептион
ms.date: 11/04/2016
f1_keywords:
- CUserException
helpviewer_keywords:
- operations [MFC], stopping
- exceptions [MFC], throwing
- CUserException class [MFC]
- errors [MFC], trapping
- operations [MFC]
- throwing exceptions [MFC], stopping user operations
ms.assetid: 2156ba6d-2cce-415a-9000-6f02c26fcd7d
ms.openlocfilehash: 6104aa2883a80f88aed03634f09ad1947e9c6794
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97344969"
---
# <a name="cuserexception-class"></a>Класс Кусерексцептион

Создается для остановки операции пользователя.

## <a name="syntax"></a>Синтаксис

```
class CUserException : public CSimpleException
```

## <a name="remarks"></a>Remarks

Используется `CUserException` , если необходимо использовать механизм исключения Throw/catch для исключений конкретного приложения. "User" в имени класса можно интерпретировать как "пользователь сделал что-то недействительное, что мне нужно обработать".

`CUserException`Обычно создается после вызова глобальной функции `AfxMessageBox` для уведомления пользователя о том, что операция завершилась ошибкой. При написании обработчика исключений следует обрабатывайте исключение, так как обычно пользователь уже уведомлен об ошибке. В некоторых случаях платформа создает это исключение. Чтобы создать `CUserException` себя, предупредите пользователя, а затем вызовите глобальную функцию `AfxThrowUserException` .

В приведенном ниже примере функция, содержащая операции, которые могут вызвать сбой, предупреждает пользователя и создает исключение `CUserException` . Вызывающая функция перехватывает исключение и обрабатывает его:

[!code-cpp[NVC_MFCExceptions#24](../../mfc/codesnippet/cpp/cuserexception-class_1.cpp)]

Дополнительные сведения об использовании см `CUserException` . в статье [обработка исключений (MFC)](../../mfc/exception-handling-in-mfc.md).

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

[CException](../../mfc/reference/cexception-class.md)

[CSimpleException](../../mfc/reference/csimpleexception-class.md)

`CUserException`

## <a name="requirements"></a>Требования

**Заголовок:** afxwin.h

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Класс CException](../../mfc/reference/cexception-class.md)
