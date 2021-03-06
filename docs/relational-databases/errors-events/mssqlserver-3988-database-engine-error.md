---
description: MSSQLSERVER_3988
title: MSSQLSERVER_3988
ms.custom: ''
ms.date: 12/25/2020
ms.prod: sql
ms.reviewer: ramakoni1, pijocoder, suresh-kandoth, vencher, tejasaks, docast
ms.technology: supportability
ms.topic: language-reference
helpviewer_keywords:
- 3988 (Database Engine error)
ms.assetid: ''
author: suresh-kandoth
ms.author: ramakoni
ms.openlocfilehash: 46070023b397f949971cf35a7c6ced936fc91e6d
ms.sourcegitcommit: d819173fb91af6f20ca6ee59686c35c71b060fbc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/28/2020
ms.locfileid: "97797766"
---
# <a name="mssqlserver_3988"></a>MSSQLSERVER_3988
 [!INCLUDE [SQL Server](../../includes/applies-to-version/sqlserver.md)]

## <a name="details"></a>详细信息

|Attribute|值|
|---|---|
|产品名称|SQL Server|
|事件 ID|3988|
|事件源|MSSQLSERVER|
|组件|SQLEngine|
|符号名称|XACT_UNSUPPORT_PARALLEL_TRAN2|
|消息正文|不允许启动新事务，因为有其他线程正在该会话中运行。|
||

## <a name="explanation"></a>说明

如果执行的分布式查询联接 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 的远程实例承载的多个表，同时 `XACT_ABORT` 会话设置为“开”，则会出现此错误。 将向用户报告如下错误消息：

> 消息 3988，级别 16，状态 1，行 #  
不允许启动新事务，因为有其他线程正在该会话中运行。

## <a name="cause"></a>原因

当满足以下条件时，[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 处理分布式查询 (DQ) 的方式存在一些设计限制：

- SQL Server 联接一个远程 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] 数据源的多个表。
- 正在发出查询的会话未在分布式事务中登记。

在这种情况下，尝试运行查询可能会引发“说明”部分中提到的两个错误。

## <a name="user-action"></a>用户操作

若要解决此问题，请将分布式查询包含在“begin distributed transaction”语句中：

```sql
BEGIN DISTRIBUTED TRANSACTION <Distributed Query> COMMIT TRANSACTION
```
