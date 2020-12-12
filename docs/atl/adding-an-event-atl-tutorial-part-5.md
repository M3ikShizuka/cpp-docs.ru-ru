---
description: 'Дополнительные сведения: Добавление события (учебник ATL, часть 5)'
title: Добавление события (учебник ATL, часть 5)
ms.custom: get-started-article
ms.date: 09/27/2018
ms.assetid: 2de12022-3148-4ce3-8606-8a9d4274f0e9
ms.openlocfilehash: 70c3b570eefa274d2cab9e31420729949d4c7974
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97166256"
---
# <a name="adding-an-event-atl-tutorial-part-5"></a>Добавление события (учебник ATL, часть 5)

На этом шаге вы добавите `ClickIn` `ClickOut` событие и в элемент управления ATL. Событие будет запущено, `ClickIn` Если пользователь щелкнет внутри многоугольника и срабатывает, `ClickOut` Если пользователь щелкнет за пределами. Ниже приведены задачи по добавлению события.

- Добавление `ClickIn` методов и `ClickOut`

- Создание библиотеки типов

- Реализация интерфейсов точек подключения

## <a name="adding-the-clickin-and-clickout-methods"></a>Добавление методов Click и Click

При создании элемента управления ATL на шаге 2 установлен флажок **точки соединения** . Этот интерфейс создан `_IPolyCtlEvents` в файле Polygon. idl. Обратите внимание, что имя интерфейса начинается с символа подчеркивания. Это соглашение указывает, что интерфейс является внутренним интерфейсом. Таким же программам, которые позволяют просматривать COM-объекты, можно не отображать интерфейс для пользователя. Также обратите внимание, что при выборе **точек подключения** в файле Polygon. idl была добавлена следующая строка, указывающая, что `_IPolyCtlEvents` является исходным интерфейсом по умолчанию:

`[default, source] dispinterface _IPolyCtlEvents;`

Атрибут Source указывает, что элемент управления является источником уведомлений, поэтому он будет вызывать этот интерфейс в контейнере.

Теперь добавьте в `ClickIn` `ClickOut` интерфейс методы и `_IPolyCtlEvents` .

### <a name="to-add-the-clickin-and-clickout-methods"></a>Добавление методов Click и Click

1. В **Обозреватель решений** откройте Polygon. idl и добавьте в `methods:` `dispInterface_IPolyCtlEvents` объявление библиотеки полигонлиб следующий код:

    ```cpp
   [id(1), helpstring("method ClickIn")] void ClickIn([in] LONG x,[in] LONG y);
   [id(2), helpstring("method ClickOut")] void ClickOut([in] LONG x,[in] LONG y);
    ```

`ClickIn`Методы и `ClickOut` принимают координаты x и y нажатой точки в качестве параметров.

## <a name="generating-the-type-library"></a>Создание библиотеки типов

Создание библиотеки типов на этом этапе, поскольку проект будет использовать его для получения сведений, необходимых для создания интерфейса точки подключения и интерфейса контейнера точки подключения для элемента управления.

### <a name="to-generate-the-type-library"></a>Создание библиотеки типов

1. Перестройте свой проект.

     -или-

1. Щелкните правой кнопкой мыши файл Polygon. idl в **Обозреватель решений** и в контекстном меню выберите команду **компилировать** .

Будет создан файл Polygon. tlb, который является библиотекой типов. Файл Polygon. tlb не отображается в **Обозреватель решений**, так как он является двоичным файлом и не может быть просмотрен или изменен напрямую.

## <a name="implementing-the-connection-point-interfaces"></a>Реализация интерфейсов точек подключения

Реализуйте интерфейс точки подключения и интерфейс контейнера точки подключения для элемента управления. В COM события реализуются с помощью механизма точек соединения. Для получения событий из COM-объекта контейнер устанавливает связь с точкой соединения, которую реализует COM-объект. Так как COM-объект может иметь несколько точек подключения, COM-объект также реализует интерфейс контейнера точки подключения. С помощью этого интерфейса контейнер может определить, какие точки подключения поддерживаются.

Вызывается интерфейс, реализующий точку подключения `IConnectionPoint` , и вызывается интерфейс, реализующий контейнер точки подключения `IConnectionPointContainer` .

Чтобы упростить реализацию `IConnectionPoint` , используйте мастер реализации точки подключения. Этот мастер создает `IConnectionPoint` интерфейс, считывая библиотеку типов и реализуя функцию для каждого события, которое может быть запущено.

### <a name="to-implement-the-connection-points"></a>Реализация точек подключения

1. В **Обозреватель решений** откройте _IPolyCtlEvents_CP. h и добавьте следующий код в `public:` оператор в `CProxy_IPolyCtlEvents` классе:

    ```cpp
    VOID Fire_ClickIn(LONG x, LONG y)
    {
        T* pT = static_cast<T*>(this);
        int nConnectionIndex;
        CComVariant* pvars = new CComVariant[2];
        int nConnections = m_vec.GetSize();

        for (nConnectionIndex = 0; nConnectionIndex < nConnections; nConnectionIndex++)
        {
            pT->Lock();
            CComPtr<IUnknown> sp = m_vec.GetAt(nConnectionIndex);
            pT->Unlock();
            IDispatch* pDispatch = reinterpret_cast<IDispatch*>(sp.p);
            if (pDispatch != NULL)
            {
                pvars[1].vt = VT_I4;
                pvars[1].lVal = x;
                pvars[0].vt = VT_I4;
                pvars[0].lVal = y;
                DISPPARAMS disp = { pvars, NULL, 2, 0 };
                pDispatch->Invoke(0x1, IID_NULL, LOCALE_USER_DEFAULT, DISPATCH_METHOD, &disp, NULL, NULL, NULL);
            }
        }
        delete[] pvars;

    }
    VOID Fire_ClickOut(LONG x, LONG y)
    {
        T* pT = static_cast<T*>(this);
        int nConnectionIndex;
        CComVariant* pvars = new CComVariant[2];
        int nConnections = m_vec.GetSize();

        for (nConnectionIndex = 0; nConnectionIndex < nConnections; nConnectionIndex++)
        {
            pT->Lock();
            CComPtr<IUnknown> sp = m_vec.GetAt(nConnectionIndex);
            pT->Unlock();
            IDispatch* pDispatch = reinterpret_cast<IDispatch*>(sp.p);
            if (pDispatch != NULL)
            {
                pvars[1].vt = VT_I4;
                pvars[1].lVal = x;
                pvars[0].vt = VT_I4;
                pvars[0].lVal = y;
                DISPPARAMS disp = { pvars, NULL, 2, 0 };
                pDispatch->Invoke(0x2, IID_NULL, LOCALE_USER_DEFAULT, DISPATCH_METHOD, &disp, NULL, NULL, NULL);
            }
        }
        delete[] pvars;

    }
    ```

Вы увидите, что этот файл содержит класс `CProxy_IPolyCtlEvents` , производный от `IConnectionPointImpl` . _IPolyCtlEvents_CP. h теперь определяет два метода `Fire_ClickIn` и `Fire_ClickOut` , которые принимают два параметра координат. Эти методы вызываются, когда требуется запустить событие из элемента управления.

При создании выбранного параметра «элемент управления с **точками соединения** » файл _IPolyCtlEvents_CP. h был создан автоматически. Он также добавляется `CProxy_PolyEvents` `IConnectionPointContainerImpl` в список множественного наследования элемента управления и предоставляется `IConnectionPointContainer` для вас путем добавления соответствующих записей в карту com.

Реализация кода для поддержки событий завершена. Теперь добавьте код для запуска событий в соответствующий момент времени. Помните, что вы будете запускать `ClickIn` событие или, `ClickOut` когда пользователь нажимает на элемент управления левую кнопку мыши. Чтобы узнать, когда пользователь нажимает кнопку, добавьте обработчик для `WM_LBUTTONDOWN` сообщения.

### <a name="to-add-a-handler-for-the-wm_lbuttondown-message"></a>Добавление обработчика для сообщения WM_LBUTTONDOWN

1. В **представление классов** щелкните правой кнопкой мыши `CPolyCtl` класс и выберите пункт **Свойства** в контекстном меню.

1. В окне **Свойства** щелкните значок **сообщения** , а затем щелкните `WM_LBUTTONDOWN` из списка слева.

1. В открывшемся раскрывающемся списке щелкните **\<Add> онлбуттондовн**. `OnLButtonDown`Объявление обработчика будет добавлено в поликтл. h, и реализация обработчика будет добавлена в поликтл. cpp.

Затем измените обработчик.

### <a name="to-modify-the-onlbuttondown-method"></a>Изменение метода Онлбуттондовн

1. Измените код, который состоит из `OnLButtonDown` метода в поликтл. cpp (удаление любого кода, помещенного мастером), так, чтобы он выглядел следующим образом:

    [!code-cpp[NVC_ATL_Windowing#57](../atl/codesnippet/cpp/adding-an-event-atl-tutorial-part-5_2.cpp)]

Этот код использует точки, вычисленные в функции, `OnDraw` для создания региона, который обнаруживает щелчки мыши пользователя с помощью вызова `PtInRegion` .

Параметр *uiacp* является идентификатором обрабатываемого сообщения Windows. Это позволяет использовать одну функцию, обрабатывающую диапазон сообщений. Параметры *wParam* и *lParam* являются стандартными значениями обрабатываемого сообщения. Параметр *бхандлед* позволяет указать, должна ли функция обрабатывать сообщение. По умолчанию значение равно TRUE, чтобы указать, что функция обработала сообщение, но можно задать для него значение FALSE. Это приведет к тому, что библиотека ATL продолжит поиск другой функции обработчика сообщений для отправки сообщения.

## <a name="building-and-testing-the-control"></a>Сборка и тестирование элемента управления

Теперь попробуйте свои события. Постройте элемент управления и снова запустите тестовый контейнер элемента управления ActiveX. На этот раз просмотрите окно Журнал событий. Чтобы направить события в окно вывода, выберите пункт **ведение журнала** в меню **Параметры** и выберите пункт **Журнал в окне вывода**. Вставьте элемент управления и попробуйте щелкнуть его в окне. Обратите внимание, что `ClickIn` срабатывает, если щелкнуть внутри закрашенного многоугольника и `ClickOut` срабатывает при щелчке за его пределами.

Далее предстоит добавить страницу свойств.

[Вернитесь к шагу 4](../atl/changing-the-drawing-code-atl-tutorial-part-4.md) &#124; [на шаг 6](../atl/adding-a-property-page-atl-tutorial-part-6.md) .

## <a name="see-also"></a>См. также раздел

[Руководство](../atl/active-template-library-atl-tutorial.md)
