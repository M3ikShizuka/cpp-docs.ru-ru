---
title: "Класс bad_function_call | Документы Майкрософт"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- functional/std::bad_function_call
dev_langs:
- C++
helpviewer_keywords:
- bad_function_call class
ms.assetid: b70a0268-43ff-4f3b-a283-faf1cb172d4c
caps.latest.revision: 20
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 65f4e356ad0d46333b0d443d0fd6ac0b9f2b6f58
ms.openlocfilehash: c6aa47c6eb3d9fc39eed6b68856641cd86d27ba5
ms.contentlocale: ru-ru
ms.lasthandoff: 10/03/2017

---
# <a name="badfunctioncall-class"></a>Класс bad_function_call
Сообщает о недопустимом вызове функции.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
class bad_function_call  
 : public std::exception {  
 };  
```  
  
## <a name="remarks"></a>Примечания  
 Данный класс описывает создание исключения для указания, что вызывается `operator()` в [классе function](../standard-library/function-class.md).
