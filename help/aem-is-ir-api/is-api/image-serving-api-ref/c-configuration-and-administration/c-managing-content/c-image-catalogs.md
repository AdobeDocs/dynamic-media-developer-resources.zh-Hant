---
description: 影像目錄提供許多伺服器組態設定，以及字型、ICC設定檔、指令巨集。
solution: Experience Manager
title: 影像目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
TQID: 'https://experienceleague.adobe.com/kfojwk0K5RfRtZdxJmdojqsLirnP6LoXbtFRJ5272lg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# 影像目錄{#image-catalogs}

影像目錄提供許多伺服器組態設定，以及字型、ICC設定檔、指令巨集。

這些功能會將要求中使用的影像和靜態內容ID對應至實際檔案路徑、儲存各種影像中繼資料（例如影像地圖），並提供範本和影像集的容器。

影像目錄只能由[!DNL Platform Server]存取，不能由影像伺服器存取。 目錄屬性檔案必須有.ini尾碼，並且置於[!DNL Platform Server]的目錄資料夾( `PS::CatalogFolder`)。 至少需要預設影像目錄，且必須填入所有屬性，才能使[!DNL Platform Server]正確運作。
