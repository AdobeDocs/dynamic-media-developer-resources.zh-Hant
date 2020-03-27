---
description: 'null'
seo-description: 'null'
seo-title: ipsApiFault
solution: Experience Manager
title: ipsApiFault
topic: Scene7 Image Production System API
uuid: 010814a8-1d29-4b02-8449-cb26e4335e07
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ipsApiFault{#ipsapifault}

語法

## 故障類型 {#section-425697675cac4b2ab5c48bd463956401}

| ID | 故障 |
|---|---|
| 30000 | `IPS_API_FAULT_CODE_EXCEPTION` |
| 30001 | `IPS_API_FAULT_CODE_INVALID_PARAMETER` |
| 30002 | `IPS_API_FAULT_CODE_MISSING_PARAMETER` |
| 30003 | `IPS_API_FAULT_CODE_INVALID_REQUEST_XML` |

## 故障欄位 {#section-37fe1aef1d5f4ca480071ca933aba826}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `code` | `xsd:int` | 故障ID |
| `reason` | `xsd:string` | 描述故障的資訊性消息。 |

