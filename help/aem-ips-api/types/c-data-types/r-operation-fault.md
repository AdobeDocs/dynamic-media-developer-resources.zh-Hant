---
description: 回應CDN失效請求中提供的其中一個URL的詳細訊息。
solution: Experience Manager
title: 操作錯誤
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
TQID: 'https://experienceleague.adobe.com/1pOPC31lIN9SI3L1hBa1Ssm9ExFEnR6wFTFam8zIbNo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 51
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

