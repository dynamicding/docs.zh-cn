---
title: "如何：创建具有访问键和文本换行的控件"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- access keys [WPF], control for
- controls [WPF], text wrapping
- wrapping text [WPF]
- keys [WPF], control for
- controls [WPF], access keys
- text wrapping [WPF]
ms.assetid: 205099d9-2551-4302-a25e-a15af9f67e04
caps.latest.revision: "22"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: c8ef62b06e97e5db22fde0085e21d7a998bfdf22
ms.sourcegitcommit: c0dd436f6f8f44dc80dc43b07f6841a00b74b23f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/19/2018
---
# <a name="how-to-create-a-control-that-has-an-access-key-and-text-wrapping"></a>如何：创建具有访问键和文本换行的控件
此示例演示如何创建具有访问键且支持文本换行的控件。 该示例使用<xref:System.Windows.Controls.Label>说明这些概念的控件。  
  
## <a name="example"></a>示例  
 **将文本换行添加到标签**  
  
 <xref:System.Windows.Controls.Label>控件不支持文本换行。 如果需要一个多次换行的标签，可以嵌套其他支持文本换行的元素，并将该元素放在标签内。 下面的示例演示如何使用<xref:System.Windows.Controls.TextBlock>进行包装若干行文本的标签。  
  
 [!code-xaml[LabelSnippet#5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LabelSnippet/CS/Pane1.xaml#5)]  
  
 **将访问键和文本换行添加到标签**  
  
 如果你需要<xref:System.Windows.Controls.Label>具有的访问密钥 （助记键），则使用<xref:System.Windows.Controls.AccessText>内的元素<xref:System.Windows.Controls.Label>。  
  
 控件如<xref:System.Windows.Controls.Label>， <xref:System.Windows.Controls.Button>， <xref:System.Windows.Controls.RadioButton>， <xref:System.Windows.Controls.CheckBox>， <xref:System.Windows.Controls.MenuItem>， <xref:System.Windows.Controls.TabItem>， <xref:System.Windows.Controls.Expander>，和<xref:System.Windows.Controls.GroupBox>具有默认控件模板。 这些模板包含<xref:System.Windows.Controls.ContentPresenter>。 您可以对设置的属性之一<xref:System.Windows.Controls.ContentPresenter>是<xref:System.Windows.Controls.ContentPresenter.RecognizesAccessKey%2A>="true"，可以用于指定控件的访问密钥。  
  
 下面的示例演示如何创建<xref:System.Windows.Controls.Label>，它具有访问键，并支持文本换行。 若要启用文本换行，该示例设置<xref:System.Windows.Controls.AccessText.TextWrapping%2A>属性并使用下划线字符指定访问密钥。 （紧跟下划线字符后面的字符就是访问键。）  
  
 [!code-xaml[LabelSnippet#4](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LabelSnippet/CS/Pane1.xaml#4)]  
  
## <a name="see-also"></a>请参阅  
 [如何：设置 Label 的目标属性](http://msdn.microsoft.com/library/b24c6977-ebcb-4855-a9bb-3fd4435af8f8)
