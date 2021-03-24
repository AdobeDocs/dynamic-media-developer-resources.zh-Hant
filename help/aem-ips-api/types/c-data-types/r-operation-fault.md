---
description: 回應CDN失效請求中提供之一URL的詳細訊息。
solution: Experience Manager
title: OperationFault
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 10%

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

