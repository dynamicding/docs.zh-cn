---
title: "其他控件结构 (Visual Basic)"
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- statements [Visual Basic], control flow
- control structures [Visual Basic]
ms.assetid: 24b811f7-98ba-40ec-8dd3-4d528cfa4574
caps.latest.revision: "19"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 09e59d25b3b2fc89026295e8500c30dad7b75086
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="other-control-structures-visual-basic"></a>其他控件结构 (Visual Basic)
[!INCLUDE[vbprvb](~/includes/vbprvb-md.md)]提供帮助你的控制结构释放资源，或减少你需要重复操作的对象引用的次数。  
  
## <a name="usingend-using-construction"></a>使用...结束使用构造  
 `Using...End Using`构造建立可在其中一个语句块使用的资源，例如 SQL 连接。 您可以根据需要获取的资源`Using`语句。 当您退出`Using`块， [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] ，以便它不用于其他代码以使用自动释放资源。 资源必须是本地且可释放。 有关详细信息，请参阅 [Using 语句](../../../../visual-basic/language-reference/statements/using-statement.md)。  
  
## <a name="withend-with-construction"></a>使用...以构造结尾  
 `With...End With`构造，可以一次指定的对象引用，然后运行一系列访问其成员的语句。 这可以简化你的代码并提高性能，因为[!INCLUDE[vbprvb](~/includes/vbprvb-md.md)]不必重新建立访问它的每个语句的引用。 有关详细信息，请参阅[与...使用语句结束](../../../../visual-basic/language-reference/statements/with-end-with-statement.md)。  
  
## <a name="see-also"></a>另请参阅  
 [控制流](../../../../visual-basic/programming-guide/language-features/control-flow/index.md)  
 [决策结构](../../../../visual-basic/programming-guide/language-features/control-flow/decision-structures.md)  
 [循环结构](../../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)  
 [嵌套的控件结构](../../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)  
 [Using 语句](../../../../visual-basic/language-reference/statements/using-statement.md)  
 [With...End With 语句](../../../../visual-basic/language-reference/statements/with-end-with-statement.md)
