---
title: 資源根資料夾(ir.resourceRootPaths)
description: 路徑清單（以分號分隔）可作為具有相對檔案路徑的所有資料檔案的根。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# 資源根資料夾(ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

路徑清單（以分號分隔）可作為具有相對檔案路徑的所有資料檔案的根。

路徑可以是絕對路徑，也可以是相對於 *[!DNL install_folder]*. 指定多個路徑時，伺服器會依指定順序嘗試每個根目錄，直到找到檔案為止。 預設值為 [!DNL ./resources]，代表預設根路徑 [!DNL install_folder/resources].
