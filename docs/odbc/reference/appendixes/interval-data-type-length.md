---
description: 间隔数据类型长度
title: 间隔数据类型长度 |Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.technology: connectivity
ms.topic: conceptual
helpviewer_keywords:
- data types [ODBC], interval data types
- length of data types [ODBC]
- interval data type [ODBC], length
ms.assetid: e9eb38d8-f9db-4401-8c62-aa394054cbbf
author: David-Engel
ms.author: v-daenge
ms.openlocfilehash: 589a13e0f0b2c6e6e42ade0f0dc32415556a0efc
ms.sourcegitcommit: e700497f962e4c2274df16d9e651059b42ff1a10
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/17/2020
ms.locfileid: "88483274"
---
# <a name="interval-data-type-length"></a>间隔数据类型长度
以下规则用于确定间隔数据类型的长度（字符）。 长度用字符数表示。 字节数取决于字符集。 长度包含同时添加的以下值：  
  
-   间隔中的每个字段都不是前导字段，两个字符。  
  
-   对于前导字段，是表示快速或隐式前导精度的字符数。 如果未指定前导精度，则默认值为2。  
  
-   字段之间的分隔符为一个字符。  
  
-   一，加上一个表达或隐含的秒精度。 如果未指定秒精度，则默认值为6。  
  
 每个间隔数据类型的特定列长度值都包含在 [列大小](../../../odbc/reference/appendixes/column-size.md)中。
