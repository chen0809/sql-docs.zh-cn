---
description: =（赋值运算符）(Transact-SQL)
title: =（赋值运算符）(Transact SQL) | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.technology: t-sql
ms.topic: language-reference
dev_langs:
- TSQL
helpviewer_keywords:
- operators [Transact-SQL], assignment
- assignment operators [Transact-SQL]
- headings [SQL Server columns]
- relationships [SQL Server], assignment operators
- column headings [SQL Server]
ms.assetid: c3040db6-21d6-40ac-a783-82c98ec006cc
author: cawrites
ms.author: chadam
monikerRange: '>=aps-pdw-2016||=azuresqldb-current||=azure-sqldw-latest||>=sql-server-2016||>=sql-server-linux-2017||=azuresqldb-mi-current'
ms.openlocfilehash: 9b68e1d58926751166820dfe1d2c697efa6d6f7e
ms.sourcegitcommit: a9e982e30e458866fcd64374e3458516182d604c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/11/2021
ms.locfileid: "98100924"
---
# <a name="-assignment-operator-transact-sql"></a>=（赋值运算符）(Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2012-all_md](../../includes/tsql-appliesto-ss2012-all-md.md)]

  等号 (=) 是唯一的 [!INCLUDE[tsql](../../includes/tsql-md.md)] 赋值运算符。 在以下示例中，先创建一个 `@MyCounter` 变量，然后用赋值运算符将 `@MyCounter` 设置为一个表达式所返回的值。  
  
```sql  
DECLARE @MyCounter INT;  
SET @MyCounter = 1;  
```  
  
 赋值运算符也能用于在列标题和定义列值的表达式之间建立联系。 以下示例显示列标题 `FirstColumnHeading` 和 `SecondColumnHeading`。 标题为 `FirstColumnHeading` 的列中，所有行均显示字符串 `xyz`。 然后，标题为`SecondColumnHeading` 的列中，列出来自 `Product` 表的每个产品 ID。  
  
```sql  
-- Uses AdventureWorks  
  
SELECT FirstColumnHeading = 'xyz',  
       SecondColumnHeading = ProductID  
FROM Production.Product;  
GO  
```  
  
## <a name="see-also"></a>另请参阅  
 [运算符 (Transact-SQL)](../../t-sql/language-elements/operators-transact-sql.md)   
 [复合运算符 (Transact-SQL)](../../t-sql/language-elements/compound-operators-transact-sql.md)   
 [表达式 (Transact-SQL)](../../t-sql/language-elements/expressions-transact-sql.md)  
  
  
