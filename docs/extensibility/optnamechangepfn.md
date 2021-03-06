---
title: "OPTNAMECHANGEPFN | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "OPTNAMECHANGEPFN"
helpviewer_keywords: 
  - "OPTNAMECHANGEPFN callback function"
ms.assetid: 147303f3-c7f1-438a-81b7-db891ea3d076
caps.latest.revision: 11
ms.author: "gregvanl"
manager: "ghogen"
---
# OPTNAMECHANGEPFN
This is a callback function specified in a call to the [SccSetOption](../extensibility/sccsetoption-function.md) (using option `SCC_OPT_NAMECHANGEPFN`) and is used to communicate name changes made by the source control plug-in back to the IDE.  
  
## Signature  
  
```cpp  
typedef void (*OPTNAMECHANGEPFN)(  
   LPVOID pvCallerData,  
   LPCSTR pszOldName,  
   LPCSTR pszNewName  
);  
```  
  
## Parameters  
 pvCallerData  
 [in] User value specified in a previous call to the [SccSetOption](../extensibility/sccsetoption-function.md) (using option `SCC_OPT_USERDATA`).  
  
 pszOldName  
 [in] The original name of the file.  
  
 pszNewName  
 [in] The name the file was renamed to.  
  
## Return Value  
 None.  
  
## Remarks  
 If a file is renamed during a source control operation, the source control plug-in can notify the IDE about the name change through this callback.  
  
 If the IDE does not support this callback, it will not call the [SccSetOption](../extensibility/sccsetoption-function.md) to specify it. If the plug-in does not support this callback, it will return `SCC_E_OPNOTSUPPORTED` from the `SccSetOption` function when the IDE attempts to set the callback.  
  
## See Also  
 [Callback Functions Implemented by the IDE](../extensibility/callback-functions-implemented-by-the-ide.md)   
 [SccSetOption](../extensibility/sccsetoption-function.md)