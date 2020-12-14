---
description: 'Дополнительные сведения о: Кусертулсманажер Class'
title: Класс Кусертулсманажер
ms.date: 11/04/2016
f1_keywords:
- CUserToolsManager
- AFXUSERTOOLSMANAGER/CUserToolsManager
- AFXUSERTOOLSMANAGER/CUserToolsManager::CUserToolsManager
- AFXUSERTOOLSMANAGER/CUserToolsManager::CreateNewTool
- AFXUSERTOOLSMANAGER/CUserToolsManager::FindTool
- AFXUSERTOOLSMANAGER/CUserToolsManager::GetArgumentsMenuID
- AFXUSERTOOLSMANAGER/CUserToolsManager::GetDefExt
- AFXUSERTOOLSMANAGER/CUserToolsManager::GetFilter
- AFXUSERTOOLSMANAGER/CUserToolsManager::GetInitialDirMenuID
- AFXUSERTOOLSMANAGER/CUserToolsManager::GetMaxTools
- AFXUSERTOOLSMANAGER/CUserToolsManager::GetToolsEntryCmd
- AFXUSERTOOLSMANAGER/CUserToolsManager::GetUserTools
- AFXUSERTOOLSMANAGER/CUserToolsManager::InvokeTool
- AFXUSERTOOLSMANAGER/CUserToolsManager::IsUserToolCmd
- AFXUSERTOOLSMANAGER/CUserToolsManager::LoadState
- AFXUSERTOOLSMANAGER/CUserToolsManager::MoveToolDown
- AFXUSERTOOLSMANAGER/CUserToolsManager::MoveToolUp
- AFXUSERTOOLSMANAGER/CUserToolsManager::RemoveTool
- AFXUSERTOOLSMANAGER/CUserToolsManager::SaveState
- AFXUSERTOOLSMANAGER/CUserToolsManager::SetDefExt
- AFXUSERTOOLSMANAGER/CUserToolsManager::SetFilter
helpviewer_keywords:
- CUserToolsManager [MFC], CUserToolsManager
- CUserToolsManager [MFC], CreateNewTool
- CUserToolsManager [MFC], FindTool
- CUserToolsManager [MFC], GetArgumentsMenuID
- CUserToolsManager [MFC], GetDefExt
- CUserToolsManager [MFC], GetFilter
- CUserToolsManager [MFC], GetInitialDirMenuID
- CUserToolsManager [MFC], GetMaxTools
- CUserToolsManager [MFC], GetToolsEntryCmd
- CUserToolsManager [MFC], GetUserTools
- CUserToolsManager [MFC], InvokeTool
- CUserToolsManager [MFC], IsUserToolCmd
- CUserToolsManager [MFC], LoadState
- CUserToolsManager [MFC], MoveToolDown
- CUserToolsManager [MFC], MoveToolUp
- CUserToolsManager [MFC], RemoveTool
- CUserToolsManager [MFC], SaveState
- CUserToolsManager [MFC], SetDefExt
- CUserToolsManager [MFC], SetFilter
ms.assetid: bdfa37ae-efca-4616-abb5-9d0dcd2d335b
ms.openlocfilehash: 1c6b3b6ec2912a0093929ac117d878d54ed9757f
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97344956"
---
# <a name="cusertoolsmanager-class"></a>Класс Кусертулсманажер

Поддерживает коллекцию объектов [класса кусертул](../../mfc/reference/cusertool-class.md) в приложении. Пользовательский инструмент — это пункт меню, который запускает внешнее приложение. Объект `CUserToolsManager` позволяет пользователю или разработчику добавить в приложение новые пользовательские инструменты. Он поддерживает выполнение команд, связанных со средствами пользователя, а также сохраняет сведения о пользовательских средствах в реестре Windows.

## <a name="syntax"></a>Синтаксис

```
class CUserToolsManager : public CObject
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Кусертулсманажер:: Кусертулсманажер](#cusertoolsmanager)|Создает документ `CUserToolsManager`.|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[Кусертулсманажер:: Креатеневтул](#createnewtool)|Создает новое средство пользователя.|
|[Кусертулсманажер:: Финдтул](#findtool)|Возвращает указатель на `CMFCUserTool` объект, связанный с указанным идентификатором команды.|
|[Кусертулсманажер:: Жетаргументсменуид](#getargumentsmenuid)|Возвращает идентификатор ресурса, связанный с меню " **аргументы** " на вкладке " **Сервис** " диалогового окна " **Настройка** ".|
|[Кусертулсманажер:: Жетдефекст](#getdefext)|Возвращает расширение по умолчанию, используемое диалоговым окном **открытия файла** ( [CFileDialog](../../mfc/reference/cfiledialog-class.md#cfiledialog)) в поле **команда** на вкладке **Сервис** диалогового окна **Настройка** .|
|[Кусертулсманажер:: i Filter](#getfilter)|Возвращает фильтр файлов, который используется диалоговое окно **Открыть файл** ( [класс CFileDialog](../../mfc/reference/cfiledialog-class.md)) в поле **команда** на вкладке **Сервис** диалогового окна **Настройка** .|
|[Кусертулсманажер:: Жетинитиалдирменуид](#getinitialdirmenuid)|Возвращает идентификатор ресурса, связанный с **начальным меню каталога** на вкладке " **Сервис** " диалогового окна " **Настройка** ".|
|[Кусертулсманажер:: Жетмакстулс](#getmaxtools)|Возвращает максимальное число пользовательских инструментов, которые могут быть выделены в приложении.|
|[Кусертулсманажер:: Жеттулсентрикмд](#gettoolsentrycmd)|Возвращает идентификатор для заполнителя пункта меню для пользовательских инструментов.|
|[Кусертулсманажер:: Жетусертулс](#getusertools)|Возвращает ссылку на список пользовательских инструментов.|
|[Кусертулсманажер:: Инвокетул](#invoketool)|Выполняет приложение, связанное с пользовательским инструментом, имеющим указанный идентификатор команды.|
|[Кусертулсманажер:: Исусертулкмд](#isusertoolcmd)|Определяет, связан ли идентификатор команды с пользовательским инструментом.|
|[Кусертулсманажер:: LoadState](#loadstate)|Загружает сведения о пользовательских средствах из реестра Windows.|
|[Кусертулсманажер:: Моветулдовн](#movetooldown)|Перемещает указанное пользовательское средство вниз в списке средств пользователя.|
|[Кусертулсманажер:: Моветулуп](#movetoolup)|Перемещает указанное пользовательское средство вверх в списке пользовательских инструментов.|
|[Кусертулсманажер:: Ремоветул](#removetool)|Удаляет указанное пользовательское средство из приложения.|
|[Кусертулсманажер:: SaveState](#savestate)|Хранит сведения о пользовательских средствах в реестре Windows.|
|[Кусертулсманажер:: Сетдефекст](#setdefext)|Указывает расширение по умолчанию, используемое диалоговым окном **открытия файла** ( [класс CFileDialog](../../mfc/reference/cfiledialog-class.md)) в поле **команда** на вкладке **Сервис** диалогового окна **Настройка** .|
|[Кусертулсманажер:: Сетфилтер](#setfilter)|Указывает фильтр файлов, используемый диалоговым окном **открытия файла** ( [класс CFileDialog](../../mfc/reference/cfiledialog-class.md)) в поле **команда** на вкладке **Сервис** диалогового окна **Настройка** .|

## <a name="remarks"></a>Комментарии

Чтобы внедрить пользовательские средства в приложение, необходимо:

1. Зарезервируйте пункт меню и связанный идентификатор команды для записи меню средства пользователя.

2. Зарезервируйте последовательный идентификатор команды для каждого пользовательского средства, которое пользователь может определить в приложении.

3. Вызовите метод [CWinAppEx:: енаблеусертулс](../../mfc/reference/cwinappex-class.md#enableusertools) и укажите следующие параметры: идентификатор команды меню, первый идентификатор команды средства пользователя и идентификатор последней команды средства пользователя.

Для каждого приложения должен быть только один глобальный `CUserToolsManager` объект.

Пример пользовательских инструментов см. в примере проекта Висуалстудиодемо.

## <a name="example"></a>Пример

В следующем примере показано, как получить ссылку на `CUserToolsManager` объект и как создать новые пользовательские инструменты. Этот фрагмент кода является частью [демонстрационного примера Visual Studio](../../overview/visual-cpp-samples.md).

[!code-cpp[NVC_MFC_VisualStudioDemo#38](../../mfc/codesnippet/cpp/cusertoolsmanager-class_1.cpp)]

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CUserToolsManager`

## <a name="requirements"></a>Требования

**Заголовок:** афксусертулсманажер. h

## <a name="cusertoolsmanagercreatenewtool"></a><a name="createnewtool"></a> Кусертулсманажер:: Креатеневтул

Создает новое средство пользователя.

```
CUserTool* CreateNewTool();
```

### <a name="return-value"></a>Возвращаемое значение

Указатель на созданное пользовательское средство или значение NULL, если число пользовательских инструментов превысило максимальное значение. Возвращаемый тип совпадает с типом, который передается в `CWinAppEx::EnableUserTools` качестве параметра *птулртк* .

### <a name="remarks"></a>Комментарии

Этот метод находит первый доступный идентификатор команды меню в диапазоне, который предоставляется при вызове метода [CWinAppEx:: енаблеусертулс](../../mfc/reference/cwinappex-class.md#enableusertools) , и присваивает ему этот идентификатор.

Метод завершается ошибкой, если число инструментов достигло максимума. Это происходит, когда все идентификаторы команд в диапазоне назначены пользовательским инструментам. Максимальное количество инструментов можно получить, вызвав [кусертулсманажер:: жетмакстулс](#getmaxtools). Доступ к списку средств можно получить, вызвав метод [кусертулсманажер:: жетусертулс](#getusertools) .

## <a name="cusertoolsmanagercusertoolsmanager"></a><a name="cusertoolsmanager"></a> Кусертулсманажер:: Кусертулсманажер

Создает документ `CUserToolsManager`. Каждое приложение должно иметь не более одного диспетчера пользовательских инструментов.

```
CUserToolsManager();

CUserToolsManager(
    const UINT uiCmdToolsDummy,
    const UINT uiCmdFirst,
    const UINT uiCmdLast,
    CRuntimeClass* pToolRTC=RUNTIME_CLASS(CUserTool),
    UINT uArgMenuID=0,
    UINT uInitDirMenuID=0);
```

### <a name="parameters"></a>Параметры

*уикмдтулсдумми*<br/>
окне Целое число без знака, используемое платформой в качестве заполнителя для идентификатора команды в меню "средства пользователя".

*уикмдфирст*<br/>
окне Идентификатор команды для первой команды средства пользователя.

*уикмдласт*<br/>
окне Идентификатор команды для последней команды средства User.

*птулртк*<br/>
окне Класс, который создает [кусертулсманажер:: креатеневтул](#createnewtool) . С помощью этого класса можно использовать производный тип [класса кусертул](../../mfc/reference/cusertool-class.md) вместо реализации по умолчанию.

*уаргменуид*<br/>
окне Идентификатор ресурса меню всплывающего меню аргументов.

*уинитдирменуид*<br/>
окне Идентификатор ресурса меню всплывающего меню исходного каталога.

### <a name="remarks"></a>Комментарии

Не вызывайте этот конструктор. Вместо этого вызовите [CWinAppEx:: енаблеусертулс](../../mfc/reference/cwinappex-class.md#enableusertools) , чтобы включить пользовательские инструменты, и вызовите [CWinAppEx:: жетусертулсманажер](../../mfc/reference/cwinappex-class.md#getusertoolsmanager) , чтобы получить указатель на `CUserToolsManager` . Дополнительные сведения см. в разделе [определяемые пользователем средства](../../mfc/user-defined-tools.md).

## <a name="cusertoolsmanagerfindtool"></a><a name="findtool"></a> Кусертулсманажер:: Финдтул

Возвращает указатель на объект [класса кусертул](../../mfc/reference/cusertool-class.md) , связанный с указанным идентификатором команды.

```
CUserTool* FindTool(UINT uiCmdId) const;
```

### <a name="parameters"></a>Параметры

*уикмдид*<br/>
окне Идентификатор команды меню.

### <a name="return-value"></a>Возвращаемое значение

Указатель на [класс кусертул](../../mfc/reference/cusertool-class.md) или `CUserTool` производный объект, если успешно. в противном случае — null.

### <a name="remarks"></a>Комментарии

При `FindTool` успешном выполнении возвращаемый тип совпадает с типом параметра *Птулртк* для [CWinAppEx:: енаблеусертулс](../../mfc/reference/cwinappex-class.md#enableusertools).

## <a name="cusertoolsmanagergetargumentsmenuid"></a><a name="getargumentsmenuid"></a> Кусертулсманажер:: Жетаргументсменуид

Возвращает идентификатор ресурса, связанный с меню " **аргументы** " на вкладке " **Сервис** " диалогового окна " **Настройка** ".

```
UINT GetArgumentsMenuID() const;
```

### <a name="return-value"></a>Возвращаемое значение

Идентификатор ресурса меню.

### <a name="remarks"></a>Комментарии

Параметр *уаргменуид* параметра [CWinAppEx:: енаблеусертулс](../../mfc/reference/cwinappex-class.md#enableusertools) указывает идентификатор ресурса.

## <a name="cusertoolsmanagergetdefext"></a><a name="getdefext"></a> Кусертулсманажер:: Жетдефекст

Возвращает расширение по умолчанию, используемое диалоговым окном **открытия файла** ( [CFileDialog](../../mfc/reference/cfiledialog-class.md#cfiledialog)) в поле **команда** на вкладке **Сервис** диалогового окна **Настройка** .

```
const CString& GetDefExt() const;
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на `CString` объект, содержащий расширение.

## <a name="cusertoolsmanagergetfilter"></a><a name="getfilter"></a> Кусертулсманажер:: i Filter

Возвращает фильтр файлов, который используется диалоговое окно **Открыть файл** ( [класс CFileDialog](../../mfc/reference/cfiledialog-class.md)) в поле **команда** на вкладке **Сервис** диалогового окна **Настройка** .

```
const CString& GetFilter() const;
```

### <a name="return-value"></a>Возвращаемое значение

Ссылка на `CString` объект, содержащий фильтр.

## <a name="cusertoolsmanagergetinitialdirmenuid"></a><a name="getinitialdirmenuid"></a> Кусертулсманажер:: Жетинитиалдирменуид

Возвращает идентификатор ресурса, связанный с **начальным меню каталога** на вкладке " **Сервис** " диалогового окна " **Настройка** ".

```
UINT GetInitialDirMenuID() const;
```

### <a name="return-value"></a>Возвращаемое значение

Идентификатор ресурса меню.

### <a name="remarks"></a>Комментарии

Возвращенный идентификатор указывается в параметре *Уинитдирменуид* [CWinAppEx:: енаблеусертулс](../../mfc/reference/cwinappex-class.md#enableusertools).

## <a name="cusertoolsmanagergetmaxtools"></a><a name="getmaxtools"></a> Кусертулсманажер:: Жетмакстулс

Возвращает максимальное число пользовательских инструментов, которые могут быть выделены в приложении.

```
int GetMaxTools() const;
```

### <a name="return-value"></a>Возвращаемое значение

Максимальное количество пользовательских средств, которые могут быть выделены.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы получить максимальное число инструментов, которые могут быть выделены в приложении. Это число идентификаторов в диапазоне от *уикмдфирст* до параметров *уикмдласт* , передаваемых в [CWinAppEx:: енаблеусертулс](../../mfc/reference/cwinappex-class.md#enableusertools).

## <a name="cusertoolsmanagergettoolsentrycmd"></a><a name="gettoolsentrycmd"></a> Кусертулсманажер:: Жеттулсентрикмд

Возвращает идентификатор для заполнителя пункта меню для пользовательских инструментов.

```
UINT GetToolsEntryCmd() const;
```

### <a name="return-value"></a>Возвращаемое значение

Идентификатор команды заполнителя.

### <a name="remarks"></a>Комментарии

Чтобы включить пользовательские инструменты, вызовите [CWinAppEx:: енаблеусертулс](../../mfc/reference/cwinappex-class.md#enableusertools). Параметр *уикмдтулсдумми* указывает идентификатор команды для команды служебной записи. Этот метод возвращает идентификатор команды для записи средств. Когда этот идентификатор используется в меню, он заменяется списком пользовательских инструментов при появлении меню.

## <a name="cusertoolsmanagergetusertools"></a><a name="getusertools"></a> Кусертулсманажер:: Жетусертулс

Возвращает ссылку на список пользовательских инструментов.

```
const CObList& GetUserTools() const;
```

### <a name="return-value"></a>Возвращаемое значение

Константная ссылка на объект [класса коблист](../../mfc/reference/coblist-class.md) , содержащий список пользовательских инструментов.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы получить список пользовательских инструментов, поддерживаемых объектом [кусертулсманажер](../../mfc/reference/cusertoolsmanager-class.md) . Каждое пользовательское средство представлено объектом типа [кусертул](../../mfc/reference/cusertool-class.md) или типом, производным от `CUserTool` . Тип задается параметром *птулртк* при вызове [CWinAppEx:: енаблеусертулс](../../mfc/reference/cwinappex-class.md#enableusertools) для включения пользовательских средств.

## <a name="cusertoolsmanagerinvoketool"></a><a name="invoketool"></a> Кусертулсманажер:: Инвокетул

Выполняет приложение, связанное с пользовательским инструментом, имеющим указанный идентификатор команды.

```
BOOL InvokeTool(UINT uiCmdId);
```

### <a name="parameters"></a>Параметры

*уикмдид*<br/>
окне Идентификатор команды меню, связанной с пользовательским инструментом.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если команда, связанная с пользовательским инструментом, успешно выполнена. в противном случае — 0.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы выполнить приложение, связанное с пользовательским инструментом, у которого есть идентификатор команды, заданный параметром *уикмдид*.

## <a name="cusertoolsmanagerisusertoolcmd"></a><a name="isusertoolcmd"></a> Кусертулсманажер:: Исусертулкмд

Определяет, связан ли идентификатор команды с пользовательским инструментом.

```
BOOL IsUserToolCmd(UINT uiCmdId) const;
```

### <a name="parameters"></a>Параметры

*уикмдид*<br/>
окне Идентификатор команды пункта меню.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если данный идентификатор команды связан с пользовательским инструментом. в противном случае — 0.

### <a name="remarks"></a>Комментарии

Этот метод проверяет, находится ли заданный идентификатор команды в диапазоне ИДЕНТИФИКАТОРов команд. Диапазон задается при вызове [CWinAppEx:: енаблеусертулс](../../mfc/reference/cwinappex-class.md#enableusertools) для включения пользовательских инструментов.

## <a name="cusertoolsmanagerloadstate"></a><a name="loadstate"></a> Кусертулсманажер:: LoadState

Загружает сведения о пользовательских средствах из реестра Windows.

```
BOOL LoadState(LPCTSTR lpszProfileName=NULL);
```

### <a name="parameters"></a>Параметры

*лпсзпрофиленаме*<br/>
окне Путь к разделу реестра Windows.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если состояние было успешно загружено; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Этот метод загружает состояние `CUserToolsManager` объекта из реестра Windows.

Обычно этот метод не вызывается напрямую. [CWinAppEx:: LoadState](../../mfc/reference/cwinappex-class.md#loadstate) вызывает его как часть процесса инициализации рабочей области.

## <a name="cusertoolsmanagermovetooldown"></a><a name="movetooldown"></a> Кусертулсманажер:: Моветулдовн

Перемещает указанное пользовательское средство вниз в списке средств пользователя.

```
BOOL MoveToolDown(CUserTool* pTool);
```

### <a name="parameters"></a>Параметры

*птул*<br/>
окне Указывает пользовательское средство для перемещения.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если пользовательское средство было успешно перемещено; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Метод завершается ошибкой, если средство, которое указывает *птул* , не находится во внутреннем списке или если средство находится в списке последним.

## <a name="cusertoolsmanagermovetoolup"></a><a name="movetoolup"></a> Кусертулсманажер:: Моветулуп

Перемещает указанное пользовательское средство вверх в списке пользовательских инструментов.

```
BOOL MoveToolUp(CUserTool* pTool);
```

### <a name="parameters"></a>Параметры

*птул*<br/>
окне Указывает пользовательское средство для перемещения.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если пользовательское средство успешно перемещено. в противном случае — 0.

### <a name="remarks"></a>Комментарии

Метод завершается ошибкой, если в средстве, указанном параметром *птул* , нет во внутреннем списке или если средство является первым элементом средства в списке.

## <a name="cusertoolsmanagerremovetool"></a><a name="removetool"></a> Кусертулсманажер:: Ремоветул

Удаляет указанное пользовательское средство из приложения.

```
BOOL RemoveTool(CUserTool* pTool);
```

### <a name="parameters"></a>Параметры

*птул*<br/>
[вход, выход] Указатель на удаляемое пользовательское средство.

### <a name="return-value"></a>Возвращаемое значение

Значение TRUE, если средство успешно удалено. В противном случае — значение FALSE.

### <a name="remarks"></a>Комментарии

Если средство успешно удалено, этот метод удаляет *птул*.

## <a name="cusertoolsmanagersavestate"></a><a name="savestate"></a> Кусертулсманажер:: SaveState

Хранит сведения о пользовательских средствах в реестре Windows.

```
BOOL SaveState(LPCTSTR lpszProfileName=NULL);
```

### <a name="parameters"></a>Параметры

*лпсзпрофиленаме*<br/>
окне Путь к разделу реестра Windows.

### <a name="return-value"></a>Возвращаемое значение

Ненулевое значение, если состояние успешно сохранено; в противном случае — 0.

### <a name="remarks"></a>Комментарии

Метод сохраняет текущее состояние `CUserToolsManager` объекта в реестре Windows.

Обычно вызывать этот метод напрямую не требуется, [CWinAppEx:: SaveState](../../mfc/reference/cwinappex-class.md#savestate) вызывает его автоматически в рамках процесса сериализации рабочей области приложения.

## <a name="cusertoolsmanagersetdefext"></a><a name="setdefext"></a> Кусертулсманажер:: Сетдефекст

Указывает расширение по умолчанию, используемое диалоговым окном **открытия файла** ( [класс CFileDialog](../../mfc/reference/cfiledialog-class.md)) в поле **команда** на вкладке **Сервис** диалогового окна **Настройка** .

```cpp
void SetDefExt(const CString& strDefExt);
```

### <a name="parameters"></a>Параметры

*стрдефекст*<br/>
окне Текстовая строка, содержащая расширение имени файла по умолчанию.

### <a name="remarks"></a>Комментарии

Вызовите этот метод, чтобы указать расширение имени файла по умолчанию в диалоговом окне **открытия файла** , которое отображается, когда пользователь выбирает приложение, связываемое с пользовательским инструментом. Значение по умолчанию — "exe".

## <a name="cusertoolsmanagersetfilter"></a><a name="setfilter"></a> Кусертулсманажер:: Сетфилтер

Указывает фильтр файлов, используемый диалоговым окном **открытия файла** ( [класс CFileDialog](../../mfc/reference/cfiledialog-class.md)) в поле **команда** на вкладке **Сервис** диалогового окна **Настройка** .

```cpp
void SetFilter(const CString& strFilter);
```

### <a name="parameters"></a>Параметры

*стрфилтер*<br/>
окне Задает фильтр.

## <a name="see-also"></a>См. также раздел

[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[Классы](../../mfc/reference/mfc-classes.md)<br/>
[Класс CWinAppEx](../../mfc/reference/cwinappex-class.md)<br/>
[Класс Кусертул](../../mfc/reference/cusertool-class.md)
