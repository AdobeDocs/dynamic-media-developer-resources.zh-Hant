---
description: 回應CDN失效請求中提供的其中一個URL的詳細訊息。
solution: Experience Manager
title: 操作錯誤
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 5%

---

# [!DNL OperationFault]{#operationfault}

回應CDN失效請求中提供的其中一個URL的詳細訊息。

**自**&#x200B;起便支援

4.5.0，修補程式2011-02

## 參數 {#section-cf4b0c923cef4c14869319af73ace58b}

| 資&#x200B;**名稱** | 資&#x200B;**型別** | 資&#x200B;**說明** |
|---|---|---|
| 代碼 | `xsd:int` | CDN提供的錯誤碼 |
| 原因 | `xsd:string` | CDN提供的錯誤訊息 |
