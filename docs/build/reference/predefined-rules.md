---
description: 'Дополнительные сведения: предопределенные правила'
title: Предварительно определенные правила
ms.date: 11/04/2016
helpviewer_keywords:
- rules, predefined
- NMAKE program, predefined rules
- predefined rules in NMAKE
ms.assetid: 638cdc3f-4aba-4b4f-96e3-ad65b0364f12
ms.openlocfilehash: 302c649980050764d1bb2f0e9a43b785d0175a09
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "97225834"
---
# <a name="predefined-rules"></a>Предварительно определенные правила

Предопределенные правила вывода используют макросы Command и Options, предоставляемые NMAKE.

|Правило|Команда|Значение по умолчанию<br /><br /> action|Пакетная служба<br /><br /> Правило|Платформа nmake работает на|
|----------|-------------|------------------------|--------------------|----------------------------|
|.asm.exe|$ (AS) $ (АФЛАГС) $<|ML $<|Нет|x86|
|ASM. obj|$ (AS) $ (АФЛАГС)/c $<|ML/c $<|да|x86|
|.asm.exe|$ (AS) $ (АФЛАГС) $<|ml64 $<|Нет|X64|
|ASM. obj|$ (AS) $ (АФЛАГС)/c $<|ml64/c $<|да|X64|
|.c.exe|$ (CC) $ (КФЛАГС) $<|CL $<|Нет|все|
|. c. obj|$ (CC) $ (КФЛАГС)/c $<|CL/c $<|да|все|
|.cc.exe|$ (CC) $ (КФЛАГС) $<|CL $<|Нет|все|
|. CC. obj|$ (CC) $ (КФЛАГС)/c $<|CL/c $<|да|все|
|.cpp.exe|$ (CPP) $ (КППФЛАГС) $<|CL $<|Нет|все|
|. cpp. obj|$ (CPP) $ (КППФЛАГС)/c $<|CL/c $<|да|все|
|.cxx.exe|$ (CXX) $ (ККСКСФЛАГС) $<|CL $<|Нет|все|
|. CXX. obj|$ (CXX) $ (ККСКСФЛАГС)/c $<|CL/c $<|да|все|
|. rc. Res|$ (RC) $ (РФЛАГС)/r $<|Версия-кандидат/r $<|Нет|все|

## <a name="see-also"></a>См. также раздел

[Правила вывода](inference-rules.md)
