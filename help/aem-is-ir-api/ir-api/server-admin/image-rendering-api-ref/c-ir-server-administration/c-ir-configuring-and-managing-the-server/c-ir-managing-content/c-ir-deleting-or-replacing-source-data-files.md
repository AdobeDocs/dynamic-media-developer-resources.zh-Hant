---
description: 您可以在伺服器上線時，使用req=release命令取代或刪除暈映檔案，然後覆寫檔案。
solution: Experience Manager
title: 刪除或取代來源資料檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
TQID: 'https://experienceleague.adobe.com/clXDwtsKfD4WkpgNvoJoXG19WvFkcOhdjtTGmoArpv4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 207
ht-degree: 0%

---

# 刪除或取代來源資料檔案{#deleting-or-replacing-source-data-files}

您可以在伺服器上線時，使用req=release命令取代或刪除暈映檔案，然後覆寫檔案。

>[!NOTE]
>
>當轉譯器伺服器存取資料檔時，不能取代或刪除資料檔。

請記住，刪除或取代來源資料檔案只會導致轉譯伺服器關閉檔案，直到存取該暈映的下一個請求為止。 如果檔案使用量很大，則可能需要多次重試。

必須停止轉譯伺服器才能取代其他資料檔案。

當替換素材檔案或暈映時，[!DNL Platform Server]個快取專案會自動失效。 取代ICC設定檔不會使快取失效。

為了避免取代檔案的複雜性，建議為取代檔案提供一個新名稱，並更新對應的目錄專案。 這可在伺服器上線時取代任何資料檔案，並造成伺服器快取專案自動過時，不需額外介入。 此方法可用於影像目錄管理的所有資料檔案。
