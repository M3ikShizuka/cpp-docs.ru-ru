---
description: Дополнительные сведения о запуске программы в качестве локального сервера
title: Запуск программы в качестве локального сервера
ms.date: 11/04/2016
helpviewer_keywords:
- debugging [ATL], running services as local server
- ATL services, running as local servers
ms.assetid: eb9701e6-e2a8-4666-897f-0c893aec8ac7
ms.openlocfilehash: 1cdf3cef0773769318d68964b28bb60ca66666d6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97157495"
---
# <a name="running-the-program-as-a-local-server"></a>Запуск программы в качестве локального сервера

Если запуск программы в качестве службы неудобен, можно временно изменить реестр таким образом, чтобы программа выполнялась как нормальный локальный сервер. Просто переименуйте `LocalService` значение под идентификатором AppID `_LocalService` и убедитесь, что `LocalServer32` ключ в идентификаторе CLSID задан правильно. (Обратите внимание, что использование DCOMCNFG позволяет указать, что приложение должно запускаться на другом компьютере `LocalServer32` `_LocalServer32` .) Запуск программы в качестве локального сервера занимает несколько секунд при запуске, так как вызов `StartServiceCtrlDispatcher` в в `CAtlServiceModuleT::Start` течение нескольких секунд завершается сбоем.

## <a name="see-also"></a>См. также раздел

[Советы по отладке](../atl/debugging-tips.md)
