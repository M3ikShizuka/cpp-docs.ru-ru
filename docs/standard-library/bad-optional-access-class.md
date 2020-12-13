---
description: 'Дополнительные сведения о: bad_optional_access классе'
title: Класс bad_optional_access
ms.date: 08/06/2019
f1_keywords:
- optional/std::bad_optional_access
ms.openlocfilehash: e3439c53766a1890592bde8ed449f5ff2779f347
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97132760"
---
# <a name="bad_optional_access-class"></a>Класс bad_optional_access

Определяет тип объектов, создаваемых как исключения, для сообщения о ситуации, когда предпринимается попытка доступа к значению `optional` объекта, который не содержит значения.

## <a name="syntax"></a>Синтаксис

```cpp
class bad_optional_access : public exception
{
public:
    bad_optional_access() noexcept;
    bad_optional_access(const bad_optional_access&) noexcept;
    bad_optional_access& operator=(const bad_optional_access&) noexcept;
    const char* what() const noexcept override;
};
```

## <a name="see-also"></a>См. также раздел

[\<optional>](optional.md)\
[необязательный класс](optional-class.md)
