---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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

