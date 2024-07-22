---
title: AssetOperationFault
description: 包含有關批次資產作業期間產生的警告或錯誤條件的資訊。 程式碼和原因欄位會對應到錯誤訊息欄位，這些欄位原本會針對同等的非批次作業而擲回。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '90'
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
