---
description: См. Дополнительные сведения о функции элемента InitInstance
title: Функция-член InitInstance
ms.date: 11/04/2016
f1_keywords:
- InitInstance
helpviewer_keywords:
- InitInstance method [MFC]
- applications [MFC], initializing
- MFC, initializing
- initializing MFC applications
ms.assetid: 4ef09267-ff7f-4c39-91a0-57454a264f83
ms.openlocfilehash: b55c5dbd665b45c74e5990b7d40a63fcd9098a9b
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97220621"
---
# <a name="initinstance-member-function"></a>Функция-член InitInstance

Операционная система Windows позволяет запускать несколько копий одного и того же приложения. `WinMain` вызывает [InitInstance](reference/cwinapp-class.md#initinstance) при каждом запуске нового экземпляра приложения.

Стандартная `InitInstance` реализация, созданная мастером приложений MFC, выполняет следующие задачи:

- В качестве центрального действия создает шаблоны документов, которые, в свою очередь, создают документы, представления и окна фрейма. Описание этого процесса см. в разделе [Создание шаблона документа](document-template-creation.md).

- Загружает стандартные параметры файла из ini-файла или реестра Windows, включая имена последних использованных файлов.

- Регистрирует один или несколько шаблонов документов.

- Для приложения MDI создает главное окно фрейма.

- Обрабатывает командную строку для открытия документа, указанного в командной строке, или для открытия нового пустого документа.

Можно добавить собственный код инициализации или изменить код, написанный мастером.

> [!NOTE]
> Приложения MFC должны быть инициализированы как однопотоковое подразделение (STA). При вызове [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) в `InitInstance` переопределении укажите COINIT_APARTMENTTHREADED (а не COINIT_MULTITHREADED).

## <a name="see-also"></a>См. также раздел

[CWinApp: класс Application](cwinapp-the-application-class.md)
