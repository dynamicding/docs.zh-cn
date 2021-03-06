---
title: "如何：暂停 Windows 服务 (Visual Basic)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- vb
f1_keywords:
- ServiceController.Pause
helpviewer_keywords:
- Windows Service applications, pausing
- pausing Windows Service applications
ms.assetid: eddb9409-942b-46b6-a2ce-fbd4c65f2790
caps.latest.revision: 
author: ghogen
ms.author: ghogen
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 90f2b01fae057a05cc71f77cecea3fdf85c832b2
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-pause-a-windows-service-visual-basic"></a>如何：暂停 Windows 服务 (Visual Basic)
此示例使用<xref:System.ServiceProcess.ServiceController>组件暂停本地计算机上的 IIS Admin 服务。  
  
## <a name="example"></a>示例  
 [!code-vb[VbRadconService#11](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#11)]  
[!code-vb[VbRadconService#12](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#12)]  
  
 此代码示例也可作为 IntelliSense 代码片段。 代码段选择器，在位于**Windows 操作系统 > Windows 服务**。 有关详细信息，请参阅[代码片段](/visualstudio/ide/code-snippets)。  
  
## <a name="compiling-the-code"></a>编译代码  
 此示例需要：  
  
-   对 System.serviceprocess.dll 的项目引用。  
  
-   对 <xref:System.ServiceProcess> 命名空间成员的访问权限。 如果未在代码中完全限定成员名称，则添加 `Imports` 语句。 有关详细信息，请参阅 [Imports 语句（.NET 命名空间和类型）](~/docs/visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)。  
  
## <a name="robust-programming"></a>可靠编程  
 <xref:System.ServiceProcess.ServiceController.MachineName%2A>属性<xref:System.ServiceProcess.ServiceController>类是默认情况下的在本地计算机。 若要引用另一台计算机上的 Windows 服务，更改<xref:System.ServiceProcess.ServiceController.MachineName%2A>属性设置为该计算机的名称。  
  
 以下情况可能会导致异常：  
  
-   不能暂停服务。 (<xref:System.InvalidOperationException>)  
  
-   访问 API 时出错。 (<xref:System.ComponentModel.Win32Exception>)  
  
## <a name="net-framework-security"></a>.NET Framework 安全性  
 控制的服务的计算机上可能会限制通过<xref:System.ServiceProcess.ServiceControllerPermissionAccess>在中设置权限<xref:System.ServiceProcess.ServiceControllerPermission>。  
  
 服务信息的访问权限可能会限制通过<xref:System.Security.Permissions.PermissionState>在中设置权限<xref:System.Security.Permissions.SecurityPermission>。  
  
## <a name="see-also"></a>请参阅  
 <xref:System.ServiceProcess.ServiceController>  
 <xref:System.ServiceProcess.ServiceControllerStatus>  
 <xref:System.ServiceProcess.ServiceController.WaitForStatus%2A>  
 [如何：继续 Windows 服务 (Visual Basic)](../../../docs/framework/windows-services/how-to-continue-a-windows-service-visual-basic.md)
