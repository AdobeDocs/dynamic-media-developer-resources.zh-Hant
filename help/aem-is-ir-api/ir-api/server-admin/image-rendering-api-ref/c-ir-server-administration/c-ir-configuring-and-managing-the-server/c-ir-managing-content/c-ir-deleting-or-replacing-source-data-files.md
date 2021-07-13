---
description: 在伺服器上線時，可以使用req=release命令在檔案被覆蓋前替換或刪除暈映檔案。
solution: Experience Manager
title: 刪除或替換源資料檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# 刪除或替換源資料檔案{#deleting-or-replacing-source-data-files}

在伺服器上線時，可以使用req=release命令在檔案被覆蓋前替換或刪除暈映檔案。

>[!NOTE]
>
>在呈現伺服器訪問資料檔案時，不能替換或刪除資料檔案。

請記住，刪除或替換源資料檔案只會導致呈現伺服器關閉檔案，直到下一個請求訪問該暈映為止。 如果檔案使用量很大，則可能需要多次重試。

必須停止呈現伺服器才能替換其他資料檔案。

替換材料檔案或暈映時，Platform Server快取條目會自動失效。 替換ICC配置檔案不會使快取無效。

為避免替換檔案的複雜性，建議為替換檔案指定新名稱並更新相應的目錄條目。 這可在伺服器上線時取代任何資料檔案，並導致伺服器快取項目自動過期，不需額外干預。 此方法可用於由映像目錄管理的所有資料檔案。
