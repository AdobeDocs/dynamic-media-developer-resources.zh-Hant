---
description: 回應CDN失效請求中提供之一URL的詳細訊息。
seo-description: 回應CDN失效請求中提供之一URL的詳細訊息。
seo-title: OperationFault
solution: Experience Manager
title: OperationFault
topic: Dynamic Media Image Production System API
uuid: 879d025b-3269-4f87-b8bd-b7916509d077
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 9%

---


# OperationFault{#operationfault}

回應CDN失效請求中提供之一URL的詳細訊息。

**支援自**

4.5.0，修補程式2011-02

## 參數 {#section-cf4b0c923cef4c14869319af73ace58b}

| ** 名稱** | ** 類型** | ** 說明** |
|---|---|---|
| `*`代碼`*` | `xsd:int` | 從CDN提供的錯誤碼 |
| `*`原因`*` | `xsd:string` | 從CDN提供的錯誤訊息 |

