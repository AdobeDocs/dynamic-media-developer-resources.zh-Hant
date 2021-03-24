---
description: 在伺服器上線時，您可在檔案覆寫之前使用req=release命令來取代或刪除暈映檔案。
solution: Experience Manager
title: 刪除或替換源資料檔案
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員、商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# 刪除或替換源資料檔案{#deleting-or-replacing-source-data-files}

在伺服器上線時，您可在檔案覆寫之前使用req=release命令來取代或刪除暈映檔案。

>[!NOTE]
>
>在Render Server訪問資料檔案時，不能替換或刪除資料檔案。

請記住，刪除或取代來源資料檔案只會導致Render Server關閉檔案，直到下次要求存取該暈映。 如果檔案被大量使用，則可能需要多次重試。

必須停止Render Server以替換其他資料檔案。

當物料檔案或暈映被取代時，平台伺服器快取項目會自動失效。 取代ICC配置檔案不會使快取失效。

為避免替換檔案的複雜性，建議為替換檔案指定新名稱並更新相應的目錄項。 這允許在伺服器上線時取代任何資料檔案，並導致伺服器快取項目自動失效，毋需額外干預。 此方法可用於由映像目錄管理的所有資料檔案。
