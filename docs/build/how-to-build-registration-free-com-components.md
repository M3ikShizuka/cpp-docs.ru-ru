---
description: 'Подробнее о следующем: Практическое руководство. Сборка не требующих регистрации компонентов COM'
title: Практическое руководство. Сборка не требующих регистрации компонентов COM
ms.date: 11/04/2016
helpviewer_keywords:
- COM components, registration-free
ms.assetid: 7e585d6a-0314-45b2-8f1b-cae9ac4df037
ms.openlocfilehash: ddcb378989878749d170705b4808d8302523a73a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97162720"
---
# <a name="how-to-build-registration-free-com-components"></a>Практическое руководство. Сборка не требующих регистрации компонентов COM

Не требующие регистрации компоненты COM — это компоненты COM, манифесты которых встроены в библиотеки DLL.

### <a name="to-build-manifests-into-com-components"></a>Встраивание манифестов в компоненты COM

1. Откройте страницы свойств проекта для компонента COM.

1. Разверните узлы **Свойства конфигурации** и **Инструмент манифеста**.

1. Выберите страницу свойств **Вход и выход** и задайте для свойства **Внедренный манифест** значение **Да**.

1. Нажмите кнопку **ОК**.

1. Постройте решение.

## <a name="see-also"></a>См. также

[Практическое руководство. Сборка изолированных приложений, использующих компоненты СОМ](how-to-build-isolated-applications-to-consume-com-components.md)
