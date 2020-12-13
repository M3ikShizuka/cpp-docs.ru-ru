---
description: 'Подробнее о: IUnknown'
title: IUnknown
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- COM interfaces, base interface
- IUnknown interface
ms.assetid: e6b85472-e54b-4b8c-b19f-4454d6c05a8f
ms.openlocfilehash: ddfd35155162275885a1c0c842b4589fa6773a4a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97152650"
---
# <a name="iunknown"></a>IUnknown

[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) является базовым интерфейсом для каждого другого COM-интерфейса.  Этот интерфейс определяет три метода: [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)), [AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)и [Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) позволяет пользователю интерфейса запрашивать у объекта указатель на другой интерфейс. [AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) и [Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) реализуют подсчет ссылок на интерфейсе.

## <a name="see-also"></a>См. также раздел

[Введение в модель COM](../atl/introduction-to-com.md)<br/>
[IUnknown и наследование интерфейсов](/windows/win32/com/iunknown-and-interface-inheritance)
