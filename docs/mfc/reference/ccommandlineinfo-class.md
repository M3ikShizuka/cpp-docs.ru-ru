---
description: 'Дополнительные сведения о: Ккоммандлинеинфо Class'
title: Класс Ккоммандлинеинфо
ms.date: 11/04/2016
f1_keywords:
- CCommandLineInfo
- AFXWIN/CCommandLineInfo
- AFXWIN/CCommandLineInfo::CCommandLineInfo
- AFXWIN/CCommandLineInfo::ParseParam
- AFXWIN/CCommandLineInfo::m_bRunAutomated
- AFXWIN/CCommandLineInfo::m_bRunEmbedded
- AFXWIN/CCommandLineInfo::m_bShowSplash
- AFXWIN/CCommandLineInfo::m_nShellCommand
- AFXWIN/CCommandLineInfo::m_strDriverName
- AFXWIN/CCommandLineInfo::m_strFileName
- AFXWIN/CCommandLineInfo::m_strPortName
- AFXWIN/CCommandLineInfo::m_strPrinterName
- AFXWIN/CCommandLineInfo::m_strRestartIdentifier
helpviewer_keywords:
- CCommandLineInfo [MFC], CCommandLineInfo
- CCommandLineInfo [MFC], ParseParam
- CCommandLineInfo [MFC], m_bRunAutomated
- CCommandLineInfo [MFC], m_bRunEmbedded
- CCommandLineInfo [MFC], m_bShowSplash
- CCommandLineInfo [MFC], m_nShellCommand
- CCommandLineInfo [MFC], m_strDriverName
- CCommandLineInfo [MFC], m_strFileName
- CCommandLineInfo [MFC], m_strPortName
- CCommandLineInfo [MFC], m_strPrinterName
- CCommandLineInfo [MFC], m_strRestartIdentifier
ms.assetid: 3e313ddb-0a82-4991-87ac-a27feff4668c
ms.openlocfilehash: 4c26ae86608725caa61ad4d1077bed01a3f40385
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97227927"
---
# <a name="ccommandlineinfo-class"></a>Класс Ккоммандлинеинфо

Помогает в синтаксическом разборе командной строки при запуске приложения.

## <a name="syntax"></a>Синтаксис

```
class CCommandLineInfo : public CObject
```

## <a name="members"></a>Члены

### <a name="public-constructors"></a>Открытые конструкторы

|name|Описание|
|----------|-----------------|
|[Ккоммандлинеинфо:: Ккоммандлинеинфо](#ccommandlineinfo)|Конструирует объект по умолчанию `CCommandLineInfo` .|

### <a name="public-methods"></a>Открытые методы

|name|Описание|
|----------|-----------------|
|[CCommandLineInfo::ParseParam](#parseparam)|Переопределите этот обратный вызов для анализа отдельных параметров.|

### <a name="public-data-members"></a>Открытые члены данных

|Имя|Описание|
|----------|-----------------|
|[Ккоммандлинеинфо:: m_bRunAutomated](#m_brunautomated)|Указывает, что `/Automation` был найден параметр командной строки.|
|[Ккоммандлинеинфо:: m_bRunEmbedded](#m_brunembedded)|Указывает, что `/Embedding` был найден параметр командной строки.|
|[Ккоммандлинеинфо:: m_bShowSplash](#m_bshowsplash)|Указывает, должен ли отображаться экран-заставка.|
|[Ккоммандлинеинфо:: m_nShellCommand](#m_nshellcommand)|Указывает обрабатываемую команду оболочки.|
|[Ккоммандлинеинфо:: m_strDriverName](#m_strdrivername)|Указывает имя драйвера, если команда оболочки печатает в; в противном случае — пустое.|
|[Ккоммандлинеинфо:: m_strFileName](#m_strfilename)|Указывает имя файла, которое должно быть открыто или напечатано; пусто, если команда оболочки является новой или DDE.|
|[Ккоммандлинеинфо:: m_strPortName](#m_strportname)|Указывает имя порта, если команда оболочки печатает в; в противном случае — пустое.|
|[Ккоммандлинеинфо:: m_strPrinterName](#m_strprintername)|Указывает имя принтера, если команда оболочки печатает в; в противном случае — пустое.|
|[Ккоммандлинеинфо:: m_strRestartIdentifier](#m_strrestartidentifier)|Указывает уникальный идентификатор перезапуска для диспетчера перезапуска, если приложение перезапущено диспетчером перезапуска.|

## <a name="remarks"></a>Комментарии

Приложение MFC, как правило, создает локальный экземпляр этого класса в функции [InitInstance](../../mfc/reference/cwinapp-class.md#initinstance) своего объекта Application. Затем этот объект передается в [CWinApp::P арсекоммандлине](../../mfc/reference/cwinapp-class.md#parsecommandline), который многократно вызывает [парсепарам](#parseparam) для заполнения `CCommandLineInfo` объекта. `CCommandLineInfo`Затем объект передается в [CWinApp::P роцессшеллкомманд](../../mfc/reference/cwinapp-class.md#processshellcommand) для управления аргументами и флагами командной строки.

Этот объект можно использовать для инкапсуляции следующих параметров командной строки и параметров:

|Аргумент командной строки|Команда выполнена|
|----------------------------|----------------------|
|*app*|Новый файл.|
|имя файла *приложения*|Откройте файл.|
|*приложение* `/p` файлов|Печать файла на принтер по умолчанию.|
|*приложение* `/pt` Порт драйвера принтера файлов|Печать файла на указанном принтере.|
|*приложение*`/dde`|Запуск и ожидание команды DDE.|
|*приложение*`/Automation`|Запуск в качестве сервера OLE Automation.|
|*приложение*`/Embedding`|Запустите, чтобы изменить внедренный элемент OLE.|
|*приложение*`/Register`<br /><br /> *приложение*`/Regserver`|Информирует приложение о выполнении любых задач регистрации.|
|*приложение*`/Unregister`<br /><br /> *приложение*`/Unregserver`|Информирует приложение о выполнении любых задач отмены регистрации.|

Создайте класс, производный от, `CCommandLineInfo` для управления другими флагами и значениями параметров. Переопределите [парсепарам](#parseparam) , чтобы обрабатывались новые флаги.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[CObject](../../mfc/reference/cobject-class.md)

`CCommandLineInfo`

## <a name="requirements"></a>Требования

**Заголовок:** afxwin.h

## <a name="ccommandlineinfoccommandlineinfo"></a><a name="ccommandlineinfo"></a> Ккоммандлинеинфо:: Ккоммандлинеинфо

Этот конструктор создает `CCommandLineInfo` объект со значениями по умолчанию.

```
CCommandLineInfo();
```

### <a name="remarks"></a>Комментарии

По умолчанию отображается экран-заставка ( `m_bShowSplash=TRUE` ) и для выполнения команды создать в меню файл ( `m_nShellCommand` **= NewFile**).

Платформа приложений вызывает [парсепарам](#parseparam) для заполнения элементов данных этого объекта.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCDocView#54](../../mfc/codesnippet/cpp/ccommandlineinfo-class_1.cpp)]

## <a name="ccommandlineinfom_brunautomated"></a><a name="m_brunautomated"></a> Ккоммандлинеинфо:: m_bRunAutomated

Указывает, что `/Automation` флаг был найден в командной строке.

```
BOOL m_bRunAutomated;
```

### <a name="remarks"></a>Комментарии

Если значение равно TRUE, то это означает, что запускается как сервер OLE Automation.

## <a name="ccommandlineinfom_brunembedded"></a><a name="m_brunembedded"></a> Ккоммандлинеинфо:: m_bRunEmbedded

Указывает, что `/Embedding` флаг был найден в командной строке.

```
BOOL m_bRunEmbedded;
```

### <a name="remarks"></a>Комментарии

Если значение — TRUE, это означает запуск для редактирования внедренного элемента OLE.

## <a name="ccommandlineinfom_bshowsplash"></a><a name="m_bshowsplash"></a> Ккоммандлинеинфо:: m_bShowSplash

Указывает, что должен отобразиться экран-заставка.

```
BOOL m_bShowSplash;
```

### <a name="remarks"></a>Комментарии

Если значение — TRUE, это означает, что экран-заставка для этого приложения должен отображаться во время запуска. Реализация [парсепарам](#parseparam) по умолчанию задает для этого элемента данных значение true, если [m_nShellCommand](#m_nshellcommand) равен `CCommandLineInfo::FileNew` .

## <a name="ccommandlineinfom_nshellcommand"></a><a name="m_nshellcommand"></a> Ккоммандлинеинфо:: m_nShellCommand

Указывает команду оболочки для этого экземпляра приложения.

```
m_nShellCommand;
```

### <a name="remarks"></a>Комментарии

Тип этого элемента данных — следующий перечислимый тип, который определен в `CCommandLineInfo` классе.

```
enum {
    FileNew,
    FileOpen,
    FilePrint,
    FilePrintTo,
    FileDDE,
    AppRegister,
    AppUnregister,
    RestartByRestartManager,
    FileNothing = -1
    };
```

Краткое описание этих значений см. в следующем списке.

- `CCommandLineInfo::FileNew` Указывает, что в командной строке не найдено имя файла.

- `CCommandLineInfo::FileOpen` Указывает, что имя файла было найдено в командной строке и что ни один из следующих флагов не найден в командной строке: `/p` , `/pt` , `/dde` .

- `CCommandLineInfo::FilePrint` Указывает, что `/p` флаг был найден в командной строке.

- `CCommandLineInfo::FilePrintTo` Указывает, что `/pt` флаг был найден в командной строке.

- `CCommandLineInfo::FileDDE` Указывает, что `/dde` флаг был найден в командной строке.

- `CCommandLineInfo::AppRegister` Указывает, что `/Register` `/Regserver` флаг или был найден в командной строке, и приложение было запрошено для регистрации.

- `CCommandLineInfo::AppUnregister` Указывает, что `/Unregister` `/Unregserver` приложению или было предложено отменить регистрацию.

- `CCommandLineInfo::RestartByRestartManager` Указывает, что приложение было перезапущено диспетчером перезапуска.

- `CCommandLineInfo::FileNothing` Отключает отображение нового дочернего окна MDI при запуске. При разработке приложения MDI, созданные мастером приложений, отображают новое дочернее окно при запуске. Чтобы отключить эту функцию, приложение может использовать `CCommandLineInfo::FileNothing` в качестве команды оболочки при вызове [ProcessShellCommand](../../mfc/reference/cwinapp-class.md#processshellcommand). `ProcessShellCommand` вызывается `InitInstance( )` из всех `CWinApp` производных классов.

### <a name="example"></a>Пример

[!code-cpp[NVC_MFCDocView#55](../../mfc/codesnippet/cpp/ccommandlineinfo-class_2.cpp)]

## <a name="ccommandlineinfom_strdrivername"></a><a name="m_strdrivername"></a> Ккоммандлинеинфо:: m_strDriverName

Сохраняет значение третьего параметра, не являющегося флагом, в командной строке.

```
CString m_strDriverName;
```

### <a name="remarks"></a>Комментарии

Обычно этот параметр является именем драйвера принтера для команды «Печать в оболочку». Реализация [парсепарам](#parseparam) по умолчанию задает этот элемент данных только в том случае, если `/pt` флаг был найден в командной строке.

## <a name="ccommandlineinfom_strfilename"></a><a name="m_strfilename"></a> Ккоммандлинеинфо:: m_strFileName

Сохраняет значение первого параметра, не являющегося флагом, в командной строке.

```
CString m_strFileName;
```

### <a name="remarks"></a>Комментарии

Обычно этот параметр является именем открываемого файла.

## <a name="ccommandlineinfom_strportname"></a><a name="m_strportname"></a> Ккоммандлинеинфо:: m_strPortName

Сохраняет значение четвертого параметра без флага в командной строке.

```
CString m_strPortName;
```

### <a name="remarks"></a>Комментарии

Обычно этот параметр является именем порта принтера для команды Print to Shell. Реализация [парсепарам](#parseparam) по умолчанию задает этот элемент данных только в том случае, если `/pt` флаг был найден в командной строке.

## <a name="ccommandlineinfom_strprintername"></a><a name="m_strprintername"></a> Ккоммандлинеинфо:: m_strPrinterName

Сохраняет значение второго параметра, не являющегося флагом, в командной строке.

```
CString m_strPrinterName;
```

### <a name="remarks"></a>Комментарии

Обычно этот параметр является именем принтера для команды Print to Shell. Реализация [парсепарам](#parseparam) по умолчанию задает этот элемент данных только в том случае, если `/pt` флаг был найден в командной строке.

## <a name="ccommandlineinfom_strrestartidentifier"></a><a name="m_strrestartidentifier"></a> Ккоммандлинеинфо:: m_strRestartIdentifier

Уникальный идентификатор перезапуска в командной строке.

```
CString m_strRestartIdentifier;
```

### <a name="remarks"></a>Комментарии

Идентификатор перезапуска уникален для каждого экземпляра приложения.

Если диспетчер перезапуска завершает работу приложения и настроен для его перезапуска, диспетчер перезапуска выполняет приложение из командной строки с идентификатором перезапуска в качестве необязательного параметра. Когда диспетчер перезапуска использует идентификатор перезапуска, приложение может повторно открыть ранее открытые документы и восстановить автоматически сохраненные файлы.

## <a name="ccommandlineinfoparseparam"></a><a name="parseparam"></a> Ккоммандлинеинфо::P Арсепарам

Платформа вызывает эту функцию для синтаксического анализа или интерпретации отдельных параметров из командной строки. Вторая версия отличается от первой только в проектах Юникода.

```
virtual void ParseParam(
    const char* pszParam,
    BOOL bFlag,
    BOOL bLast);

virtual void ParseParam(
    const TCHAR* pszParam,
    BOOL bFlag,
    BOOL bLast);
```

### <a name="parameters"></a>Параметры

*псзпарам*<br/>
Параметр или флаг.

*бфлаг*<br/>
Указывает, является ли *псзпарам* параметром или флагом.

*bLast*<br/>
Указывает, является ли это последним параметром или флагом в командной строке.

### <a name="remarks"></a>Комментарии

[CWinApp::P арсекоммандлине](../../mfc/reference/cwinapp-class.md#parsecommandline) вызывает `ParseParam` один раз для каждого параметра или флага в командной строке, передавая аргумент в *псзпарам*. Если первым символом параметра является " **-** " или " **/** ", он удаляется, а для *БФЛАГ* устанавливается значение true. При синтаксическом анализе окончательного параметра параметру *Sound* ПРИСВАИВАЕТСЯ значение true.

Реализация по умолчанию этой функции распознает следующие флаги: `/p` , `/pt` , `/dde` , `/Automation` и `/Embedding` , как показано в следующей таблице.

|Аргумент командной строки|Команда выполнена|
|----------------------------|----------------------|
|*app*|Новый файл.|
|имя файла *приложения*|Откройте файл.|
|*приложение* `/p` файлов|Печать файла на принтер по умолчанию.|
|*приложение* `/pt` Порт драйвера принтера файлов|Печать файла на указанном принтере.|
|*приложение*`/dde`|Запуск и ожидание команды DDE.|
|*приложение*`/Automation`|Запуск в качестве сервера OLE Automation.|
|*приложение*`/Embedding`|Запустите, чтобы изменить внедренный элемент OLE.|
|*приложение*`/Register`<br /><br /> *приложение*`/Regserver`|Информирует приложение о выполнении любых задач регистрации.|
|*приложение*`/Unregister`<br /><br /> *приложение*`/Unregserver`|Информирует приложение о выполнении любых задач отмены регистрации.|

Эти сведения хранятся в [m_bRunAutomated](#m_brunautomated), [m_bRunEmbedded](#m_brunembedded)и [m_nShellCommand](#m_nshellcommand). Флаги помечены косой чертой " **/** " или дефисом " **-** ".

Реализация по умолчанию помещает первый параметр без флага в [m_strFileName](#m_strfilename). В случае с `/pt` флагом реализация по умолчанию помещает второй, третий и четвертый параметры без флагов в [m_strPrinterName](#m_strprintername), [m_strDriverName](#m_strdrivername)и [m_strPortName](#m_strportname)соответственно.

Реализация по умолчанию также устанавливает для [m_bShowSplash](#m_bshowsplash) значение true только в случае нового файла. В случае нового файла пользователь потратил действие на само приложение. В любом другом случае, включая открытие существующих файлов с помощью оболочки, пользовательское действие непосредственно включает файл. На основе документа-заставки не требуется объявлять о запуске приложения.

Переопределите эту функцию в производном классе, чтобы обрабатывались другие значения флагов и параметров.

## <a name="see-also"></a>См. также раздел

[CObject, класс](../../mfc/reference/cobject-class.md)<br/>
[Иерархическая диаграмма](../../mfc/hierarchy-chart.md)<br/>
[CWinApp::P Арсекоммандлине](../../mfc/reference/cwinapp-class.md#parsecommandline)<br/>
[CWinApp::P Роцессшеллкомманд](../../mfc/reference/cwinapp-class.md#processshellcommand)
