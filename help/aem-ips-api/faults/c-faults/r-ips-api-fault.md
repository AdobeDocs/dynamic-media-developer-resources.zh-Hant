---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 48be47f6-4c1c-4f19-afa7-f643e504c287
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '32'
ht-degree: 28%

---

# ipsApiFault{#ipsapifault}

語法

## 故障類型{#section-425697675cac4b2ab5c48bd463956401}

| ID | 故障 |
|---|---|
| 30000 | `IPS_API_FAULT_CODE_EXCEPTION` |
| 郵遞區號30001 | `IPS_API_FAULT_CODE_INVALID_PARAMETER` |
| 郵遞區號30002 | `IPS_API_FAULT_CODE_MISSING_PARAMETER` |
| 郵遞區號30003 | `IPS_API_FAULT_CODE_INVALID_REQUEST_XML` |

## 故障欄位{#section-37fe1aef1d5f4ca480071ca933aba826}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `code` | `xsd:int` | 故障ID |
| `reason` | `xsd:string` | 描述故障的資訊性消息。 |
