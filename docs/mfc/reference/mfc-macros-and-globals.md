---
description: 'Дополнительные сведения: макросы и глобальные библиотеки MFC'
title: Макросы и глобальные объекты MFC
ms.date: 11/04/2016
helpviewer_keywords:
- MFC, global functions and variables
- MFC, macros
- global functions, MFC
- macros, MFC
- global functions [MFC]
- global variables, MFC
- Afx naming convention
- macros
ms.assetid: add4e33f-0e62-4d27-be14-896cb8675d22
ms.openlocfilehash: 9e3d3acd74d1cf6db5856432cdefd632e36185f3
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97219152"
---
# <a name="mfc-macros-and-globals"></a>Макросы и глобальные объекты MFC

Библиотека Microsoft Foundation Class можно разделить на два основных раздела: (1) классы MFC и (2) макросы и глобальные. Если функция или переменная не является членом класса, это глобальная функция или переменная.

Библиотека MFC и макросы преобразования строк общего ресурса библиотеки ATL. Дополнительные сведения см. в разделе [макросы преобразования строк](../../atl/reference/string-conversion-macros.md) в документации ATL.

Макросы и глобальные классы MFC предоставляют функциональные возможности в следующих категориях.

## <a name="general-mfc"></a>Общие классы MFC

- [Типы данных](data-types-mfc.md)

- [Приведение типов объектов классов MFC](type-casting-of-mfc-class-objects.md)

- [Службы модели объекта во время выполнения](run-time-object-model-services.md)

- [Службы диагностики](diagnostic-services.md)

- [Обработка исключений](exception-processing.md)

- [Форматирование CString и отображение окна сообщения](cstring-formatting-and-message-box-display.md)

- [Схемы сообщений](message-map-macros-mfc.md)

- [Сопоставление делегатов и интерфейсов](delegate-and-interface-maps.md)

- [Модули и библиотеки DLL](extension-dll-macros.md)

- [Сведения о приложении и управление им](application-information-and-management.md)

- [Стандартная команда и идентификаторы окон](standard-command-and-window-ids.md)

- [Вспомогательные функции классов коллекции](collection-class-helpers.md)

- [Функции серого цвета и сглаживания точечного рисунка](gray-and-dithered-bitmap-functions.md)

- [Стандартные подпрограммы обмена данными в диалоговых окнах (DDX)](standard-dialog-data-exchange-routines.md)

- [Стандартные подпрограммы проверки данных в диалоговых окнах (DDV)](standard-dialog-data-validation-routines.md)

- [Сообщения AFX](afx-messages.md)

- [Стили элементов управления панели инструментов](toolbar-control-styles.md)

- [Перечисление перечисление CMFCImagePaintArea:: IMAGE_EDIT_MODE](cmfcimagepaintarea-image-edit-mode-enumeration.md)

## <a name="database"></a>База данных

- [Функции обмена полями записей (RFX)](record-field-exchange-functions.md) и [функции Многоблочного обмена полями записей (массовых RFX)](record-field-exchange-functions.md) для классов ODBC MFC

- [Функции обмена полями записи (DFX)](record-field-exchange-functions.md) для классов MFC DAO

- [Функции обмена данными диалоговых окон (DDX) для CRecordView и CDaoRecordView](dialog-data-exchange-functions-for-crecordview-and-cdaorecordview.md) (классы MFC ODBC и DAO)

- [Функции обмена данными диалоговых окон (DDX) для элементов управления OLE](dialog-data-exchange-functions-for-ole-controls.md)

- [Макросы и глобальные возможности для непосредственного вызова функций API ODBC](database-macros-and-globals.md)

- [Инициализация и прекращение работы ядра СУБД DAO](dao-database-engine-initialization-and-termination.md)

## <a name="internet"></a>Интернет

- [Глобальные объекты анализа URL-адресов](internet-url-parsing-globals.md)

## <a name="dhtml--dhtml-event-maps"></a>Сопоставления событий DHTML и DHTML

- [Вспомогательные макросы обмена диалоговыми данными DHTML (DDX)](ddx-dhtml-helper-macros.md)

- [Схемы событий DHTML](dhtml-event-maps.md)

## <a name="ole"></a>OLE

- [Инициализация OLE](ole-initialization.md)

- [управление приложениями](application-control.md);

- [Схемы подготовки к отправке](dispatch-maps.md)

Кроме того, MFC предоставляет функцию с именем [афксенаблеконтролконтаинер](ole-initialization.md#afxenablecontrolcontainer) , которая позволяет любому контейнеру OLE, разработанному с помощью MFC 4,0, полностью поддерживать внедренные элементы управления OLE.

## <a name="ole-controls"></a>Элементы управления OLE

- [Константы типа параметра Variant](variant-parameter-type-constants.md)

- [Доступ к библиотеке типов](type-library-access.md)

- [Страницы свойств](property-pages-mfc.md)

- [Схемы событий](event-maps.md)

- [Схемы приемников событий](event-sink-maps.md)

- [Схемы подключения](connection-maps.md)

- [Регистрация элементов управления OLE](registering-ole-controls.md)

- [Фабрики классов и лицензирование](class-factories-and-licensing.md)

- [Сохраняемость элементов управления OLE](persistence-of-ole-controls.md)

В первой части этого раздела кратко рассматриваются все предыдущие категории и перечислены глобальные и макросы в категории, а также краткие описания функций. Далее приведены описания глобальных функций, глобальных переменных и макросов в библиотеке MFC.

> [!NOTE]
> Многие глобальные функции начинаются с префикса «AFX», но некоторые, например, функции обмена данными диалоговых окон (DDX) и многие функции базы данных, не соответствуют этому соглашению. Все глобальные переменные начинаются с "AFX" в качестве префикса. Макросы не начинаются с какого бы то ни было определенного префикса, но записываются прописными буквами.

## <a name="see-also"></a>См. также раздел

[Общие сведения о классах](../../mfc/class-library-overview.md)
