---
title: "如何：在属性值更改时触发动画"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- animation [WPF], starting when property values change
- triggering animation [WPF]
- Storyboards [WPF], starting when property values change
ms.assetid: 12399c21-0300-4f4f-9e3a-d92d9907e5f5
caps.latest.revision: "7"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 0eb4542d8baf86f01417eb1925028a00471b40b5
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-trigger-an-animation-when-a-property-value-changes"></a>如何：在属性值更改时触发动画
此示例演示如何使用<xref:System.Windows.Trigger>启动<xref:System.Windows.Media.Animation.Storyboard>属性值更改时。 你可以使用<xref:System.Windows.Trigger>内<xref:System.Windows.Style>， <xref:System.Windows.Controls.ControlTemplate>，或<xref:System.Windows.DataTemplate>。  
  
## <a name="example"></a>示例  
 下面的示例使用<xref:System.Windows.Trigger>要进行动画处理<xref:System.Windows.UIElement.Opacity%2A>的<xref:System.Windows.Controls.Button>时其<xref:System.Windows.UIElement.IsMouseOver%2A>属性变为`true`。  
  
 [!code-xaml[AnimatePropertyStoryboards#PropertyTriggerExample](../../../../samples/snippets/xaml/VS_Snippets_Wpf/AnimatePropertyStoryboards/XAML/PropertyTriggerExample.xaml#propertytriggerexample)]  
  
 属性应用动画<xref:System.Windows.Trigger>的对象行为比更复杂的方式<xref:System.Windows.EventTrigger>动画开始使用<xref:System.Windows.Media.Animation.Storyboard>方法。  它们"提交"时使用动画定义由其他<xref:System.Windows.Trigger>对象，但 compose 与<xref:System.Windows.EventTrigger>和方法，触发动画。  
  
## <a name="see-also"></a>请参阅  
 <xref:System.Windows.Trigger>  
 [属性动画技术概述](../../../../docs/framework/wpf/graphics-multimedia/property-animation-techniques-overview.md)  
 [演示图板概述](../../../../docs/framework/wpf/graphics-multimedia/storyboards-overview.md)
