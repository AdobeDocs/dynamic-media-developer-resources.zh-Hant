---
description: 所有記錄檔都會寫入以TC目錄指定的相同記錄資料夾。
solution: Experience Manager
title: 伺服器記錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
TQID: 'https://experienceleague.adobe.com/9I1gAXWb1Rpuml9WCCVPVC7FrpVazWN79Sk0-bb-tDc'
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
source-wordcount: 170
ht-degree: 1%

---

# 伺服器記錄{#server-logging}

所有記錄檔都會寫入以TC：：directory指定的相同記錄資料夾。

通常會每天建立和旋轉記錄檔。 在指定的天數( `TC::maxDays`)後，日誌資料夾中的舊日誌檔會自動刪除。

重要須為記錄檔保留足夠的磁碟空間，以免用盡磁碟空間。 大量使用的伺服器和預設記錄檔設定可能需要1-2 GB/天。

[!DNL Platform Server]和影像伺服器會建立以下所述的三種記錄檔型別。

其他「影像伺服」元件和某些其他Dynamic Media套件（例如Dynamic Media檢視器）也可能會在相同的資料夾中建立記錄檔。 這些記錄檔供Dynamic Media內部使用，Dynamic Media技術支援可能會要求這些記錄檔以進行疑難排解。

* [存取記錄](c-access-log.md)
* [追蹤記錄](c-trace-log.md)
* [影像伺服器記錄](c-image-server-log.md)

## 另請參閱 {#section-5ff5e46031b1461c92de24e632610d6d}

[存取記錄](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f)，[偵錯/追蹤記錄](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
