---
description: Дополнительные сведения см. в статье пути поиска в правилах.
title: Пути поиска в правилах
ms.date: 11/04/2016
helpviewer_keywords:
- search paths in NMAKE inference rules
- inference rules in NMAKE
- rules, inference
ms.assetid: 38feded6-536d-425d-bf40-fff3173a5506
ms.openlocfilehash: bf070fc57907b68eb458b8a5276698282ef30f9d
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97224885"
---
# <a name="search-paths-in-rules"></a>Пути поиска в правилах

```
{frompath}.fromext{topath}.toext:
   commands
```

## <a name="remarks"></a>Комментарии

Правило вывода применяется к зависимости только в том случае, если пути, указанные в зависимости, точно соответствуют путям правила вывода. Укажите каталог зависимого объекта в *фромпас* и целевой каталог в *Топас*; пробелы не допускаются. Укажите только один путь для каждого расширения. Для пути к одному расширению требуется путь в другом. Чтобы указать текущий каталог, используйте точку (.) или пустые фигурные скобки ({}). Макросы могут представлять *фромпас* и *Топас*; они вызываются во время предварительной обработки.

## <a name="example"></a>Пример

### <a name="code"></a>Код

```
{dbi\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $(YUDBI) $<

{ilstore\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $<

{misc\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $(YUPDB) $<

{misc\}.c{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $<

{msf\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $<

{bsc\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $(YUPDB) $<

{mre\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $(YUPDB) $<

{namesrvr\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $(YUPDB) $<

{src\cvr\}.cpp{$(ODIR)}.obj::
        $(CC) $(CFLAGS) $<
```

## <a name="see-also"></a>См. также

[Определение правила](defining-a-rule.md)
