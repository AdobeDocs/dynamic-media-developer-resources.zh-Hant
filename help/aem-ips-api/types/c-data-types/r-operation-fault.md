---
description: 回應CDN失效請求中提供之一個URL的詳細訊息。
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 11%

---

# OperationFault{#operationfault}

回應CDN失效請求中提供之一個URL的詳細訊息。

**支援時間**

4.5.0，修補程式2011-02

## 參數 {#section-cf4b0c923cef4c14869319af73ace58b}

| ** 名稱** | ** 類型** | ** 說明** |
|---|---|---|
| `*`代碼`*` | `xsd:int` | 從CDN提供的錯誤代碼 |
| `*`原因`*` | `xsd:string` | 從CDN提供的錯誤訊息 |
