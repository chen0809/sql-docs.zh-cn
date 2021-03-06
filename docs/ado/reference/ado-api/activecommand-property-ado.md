---
description: ActiveCommand 属性 (ADO)
title: " (ADO) 的 ActiveCommand 属性 |Microsoft Docs"
ms.prod: sql
ms.prod_service: connectivity
ms.technology: ado
ms.custom: ''
ms.date: 01/19/2017
ms.reviewer: ''
ms.topic: conceptual
apitype: COM
f1_keywords:
- Recordset20::ActiveCommand
helpviewer_keywords:
- ActiveCommand property [ADO]
ms.assetid: fb4088d5-5968-42d6-aeaa-3955046bb4da
author: rothja
ms.author: jroth
ms.openlocfilehash: df737543e8cc09735c7da413b89406b6f2385079
ms.sourcegitcommit: 18a98ea6a30d448aa6195e10ea2413be7e837e94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/27/2020
ms.locfileid: "88977148"
---
# <a name="activecommand-property-ado"></a>ActiveCommand 属性 (ADO)
指示创建关联[记录集](./recordset-object-ado.md)对象的[命令](./command-object-ado.md)对象。  
  
## <a name="return-value"></a>返回值  
 返回一个包含**命令**对象的**变量**。 默认值为 null 对象引用。  
  
## <a name="remarks"></a>注解  
 **ActiveCommand**属性是只读的。  
  
 如果未使用 **命令** 对象创建当前 **记录集**，则返回 **Null** 对象引用。  
  
 当只给定生成的**记录集**对象时，使用此属性可查找关联的**命令**对象。  
  
## <a name="applies-to"></a>适用于  
 [记录集对象 (ADO)](./recordset-object-ado.md)  
  
## <a name="see-also"></a>另请参阅  
 [ActiveCommand 属性示例 (VB) ](./activecommand-property-example-vb.md)   
 [ActiveCommand 属性示例 (JScript) ](./activecommand-property-example-jscript.md)   
 [ActiveCommand 属性示例 (VC + +) ](./activecommand-property-example-vc.md)   
 [命令对象 (ADO)](./command-object-ado.md)