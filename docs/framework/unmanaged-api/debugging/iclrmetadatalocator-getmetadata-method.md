---
title: "ICLRMetadataLocator::GetMetadata 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- ICLRMetadataLocator.GetMetadata
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRMetadataLocator::GetMetadata
helpviewer_keywords:
- GetMetadata method, ICLRMetadataLocator interface [.NET Framework debugging]
- ICLRMetadataLocator::GetMetadata method [.NET Framework debugging]
ms.assetid: 704a8893-ac56-43b4-90ea-715f38ccb40e
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 8758a96464d1465d92fb17314f1e36ab8d9169c4
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="iclrmetadatalocatorgetmetadata-method"></a>ICLRMetadataLocator::GetMetadata 方法
调用由公共语言运行时 (CLR) 数据访问服务以检索图像的元数据。  
  
## <a name="syntax"></a>语法  
  
```  
HRESULT GetMetadata(  
    [in]  LPCWSTR         imagePath,  
    [in]  ULONG32         imageTimestamp,  
    [in]  ULONG32         imageSize,  
    [in]  GUID*           mvid,  
    [in]  ULONG32         mdRva,  
    [in]  ULONG32         flags,  
    [in]  ULONG32         bufferSize,  
    [out, size_is(bufferSize), length_is(*dataSize)]  
          BYTE*           buffer,  
    [out] ULONG32*        dataSize  
);  
```  
  
#### <a name="parameters"></a>参数  
 `imagePath`  
 [in]一个字符串，指定图像文件的路径。  
  
 `imageTimestamp`  
 [in]图像文件的时间戳。  
  
 `imageSize`  
 [in]图像文件的大小。  
  
 `mvid`  
 [in]图像的全局唯一标识符。  
  
 `mdRva`  
 [in]相对虚拟地址 (RVA) 的元数据。 该地址是相对于映像的基址。  
  
 `flags`  
 [in]留待将来使用。  
  
 `bufferSize`  
 [in]要在其中放置元数据缓冲区的大小。  
  
 `buffer`  
 [out]要在其中放置元数据缓冲区。  
  
 `dataSize`  
 [out]返回的元数据的大小。  
  
## <a name="remarks"></a>备注  
 此方法由调试应用程序的编写器实现。  
  
## <a name="requirements"></a>惠?  
 **平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** ClrData.idl、 ClrData.h  
  
 **库：** CorGuids.lib  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [ICLRMetadataLocator 接口](../../../../docs/framework/unmanaged-api/debugging/iclrmetadatalocator-interface.md)
