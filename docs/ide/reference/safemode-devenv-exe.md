---
title: "-SafeMode (devenv.exe) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "/SafeMode Devenv switch"
  - "Devenv, /SafeMode switch"
  - "SafeMode switch"
ms.assetid: b191f6a5-8f12-47ec-bcc7-b68149a22aa8
caps.latest.revision: 5
author: "gewarren"
ms.author: "gewarren"
manager: "ghogen"
---
# /SafeMode (devenv.exe)
Starts [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] in safe mode, loading only the default environment and services.  
  
## Syntax  
  
```  
devenv /SafeMode   
```  
  
## Remarks  
 This switch prevents all third-party VSPackages from loading when [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] starts, thus ensuring stable execution.  
  
## Description  
 The following example starts [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] in safe mode.  
  
## Code  
  
```  
Devenv.exe /SafeMode  
```  
  
## See Also  
 [Devenv Command Line Switches](../../ide/reference/devenv-command-line-switches.md)