---
title: "名称&lt;namespacename&gt;根命名空间中&lt;fullnamespacename&gt;不符合 CLS"
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc40039
- bc40039
helpviewer_keywords:
- BC40039
ms.assetid: c5bd5914-ae71-416a-8bed-f76f644f78be
caps.latest.revision: 
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 3a89f8cfe4038a81002777886de1155bea72ba22
ms.sourcegitcommit: 34ec7753acf76f90a0fa845235ef06663dc9e36e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="name-ltnamespacenamegt-in-the-root-namespace-ltfullnamespacenamegt-is-not-cls-compliant"></a>名称&lt;namespacename&gt;根命名空间中&lt;fullnamespacename&gt;不符合 CLS
程序集标记为`<CLSCompliant(True)>`，但根命名空间名称的元素以下划线开头 (`_`)。  
  
 编程元素可以包含一个或多个下划线，但要符合[语言独立性和独立于语言的组件](../../../standard/language-independence-and-language-independent-components.md)(CLS)，它必须不以下划线开头。 请参阅[声明的元素名称](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)。  
  
 当将 <xref:System.CLSCompliantAttribute> 应用到编程元素中时，需要将该特性的 `isCompliant` 参数设置为 `True` 或 `False` 来指示符合或不符合性。 此参数没有默认值，必须为其提供一个值。  
  
 如果不将 <xref:System.CLSCompliantAttribute> 应用到元素，则它将被视为不符合规范。  
  
 默认情况下，此消息是一个警告。 有关隐藏警告或将警告视为错误的信息，请参见 [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic)。  
  
 **错误 ID:** BC40039  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
-   如果你需要 CLS 符合性，更改根命名空间名称，以便其元素以下划线开头。  
  
-   如果你需要命名空间名称保持不变，然后删除<xref:System.CLSCompliantAttribute>从程序集或将其标记为`<CLSCompliant(False)>`。  
  
## <a name="see-also"></a>请参阅  
 [Namespace 语句](../../../visual-basic/language-reference/statements/namespace-statement.md)  
 [在 Visual Basic 中的命名空间](../../../visual-basic/programming-guide/program-structure/namespaces.md)  
 [/rootnamespace](../../../visual-basic/reference/command-line-compiler/rootnamespace.md)  
 [“项目设计器”->“应用程序”页 (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic)  
 [已声明的元素名称](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)  
 [Visual Basic 命名约定](../../../visual-basic/programming-guide/program-structure/naming-conventions.md)  
 
