---
description: 當使用者無法驗證時拋出。
solution: Experience Manager
title: authenticationFault
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 21%

---


# authenticationFault{#authenticationfault}

當使用者無法驗證時拋出。

語法

## 故障類型{#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | 故障 |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 郵遞區號10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 郵遞區號10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## 故障欄位{#section-1fe84846a7154b03ab49552810ee9ac3}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `code` | `xsd:int` | 故障ID |
| `reason` | `xsd:string` | 描述故障的資訊性消息。 |
