---
title: "轮询异步操作的状态"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- asynchronous programming, status polling
- polling asynchronous operation status
- status information [.NET Framework], asynchronous operations
ms.assetid: b541af31-dacb-4e20-8847-1b1ff7c35363
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 51e2ada4b493e8b1cbe0744c00fc2c25f9a266fb
ms.sourcegitcommit: 957c696f25e39f923a827fc3ad5e8ab72768838c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/13/2018
---
# <a name="polling-for-the-status-of-an-asynchronous-operation"></a>轮询异步操作的状态
如果应用可以在等待异步操作结果期间继续执行其他工作，不得阻止应用一直到操作完成。 请使用下列方法之一，在应用等待异步操作完成期间继续执行指令：  
  
-   使用异步操作的 BeginOperationName****** 方法返回的 <xref:System.IAsyncResult> 的 <xref:System.IAsyncResult.IsCompleted%2A> 属性，确定操作是否已完成。 这种方法称为“轮询”，本主题介绍的就是它。  
  
-   使用 <xref:System.AsyncCallback> 委托，在单独的线程中处理异步操作结果。 有关展示这种方法的示例，请参阅[使用 AsyncCallback 委托结束异步操作](../../../docs/standard/asynchronous-programming-patterns/using-an-asynccallback-delegate-to-end-an-asynchronous-operation.md)。  
  
## <a name="example"></a>示例  
 下面的代码示例展示了如何使用 <xref:System.Net.Dns> 类中的异步方法，检索用户指定计算机的域名系统信息。 此示例启动异步操作，然后在控制台打印句点 (".")，直到操作完成。 请注意，对 <xref:System.Net.Dns.BeginGetHostByName%2A><xref:System.AsyncCallback> 和 <xref:System.Object> 参数传递的是 null（Visual Basic 中的 Nothing），因为使用这种方法时这些是可选参数。  
  
 [!code-csharp[AsyncDesignPattern#3](../../../samples/snippets/csharp/VS_Snippets_CLR/AsyncDesignPattern/CS/Async_Poll.cs#3)]
 [!code-vb[AsyncDesignPattern#3](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AsyncDesignPattern/VB/Async_Poll.vb#3)]  
  
## <a name="see-also"></a>请参阅  
 [基于事件的异步模式 (EAP)](../../../docs/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-eap.md)  
 [基于事件的异步模式概述](../../../docs/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview.md)
