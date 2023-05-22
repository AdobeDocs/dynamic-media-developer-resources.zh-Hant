---
description: 路徑清單（用分號分隔）用作具有相對檔案路徑的所有資料檔案的根。
solution: Experience Manager
title: 資源根資料夾(ir.resourceRootPaths)
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# 資源根資料夾(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

路徑清單（用分號分隔）用作具有相對檔案路徑的所有資料檔案的根。

可以是絕對路徑或相對於 *[!DNL install_folder]*。 指定多個路徑後，伺服器將按給定順序嘗試每個根，直到找到該檔案。 預設值為 [!DNL ./resources]，用於的預設根路徑 [!DNL install_folder/resources]。
