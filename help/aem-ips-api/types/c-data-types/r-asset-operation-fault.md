---
title: AssetOperationFault
description: 包含有關批次資產作業期間產生的警告或錯誤條件的資訊。 程式碼和原因欄位會對應到錯誤訊息欄位，這些欄位原本會針對同等的非批次作業而擲回。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
TQID: 'https://experienceleague.adobe.com/LCiMAp-8grDIfCEGX3sF2kBhDamlxZ8iFHT1BjBLkCY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 7%

---

# [!DNL AssetOperationFault]{#assetoperationfault}

包含有關批次資產作業期間產生的警告或錯誤條件的資訊。 程式碼和原因欄位會對應到錯誤訊息欄位，這些欄位原本會針對同等的非批次作業而擲回。

語法

## 參數 {#section-c906f052f43e4785ba46d92b514b0923}

| 名稱 | 類型 | 說明 |
|---|---|---|
| assetHandle | `xsd:string` | 失敗的操作的資產控制代碼。 |
| 代碼 | `xsd:int` | 作業錯誤碼。 |
| 原因 | `xsd:string` | 錯誤說明或原因。 |

