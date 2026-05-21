---
description: 只有 [!DNL Platform Server]可存取靜態內容來源資料檔。
solution: Experience Manager
title: 靜態內容來源資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
TQID: 'https://experienceleague.adobe.com/XFhKuqGPsarkFZcYcBo7XuyCEsiJINf-o6koIZQKAXU'
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
source-wordcount: 112
ht-degree: 0%

---

# 靜態內容來源資料{#static-content-source-data}

只有[!DNL Platform Server]可存取靜態內容來源資料檔。

靜態內容資料檔案的路徑解析如下：

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

伺服器會由右至左組合路徑區段，直到建立絕對檔案路徑為止。

所有` *[!DNL rootPath]*`區段都可以是空白、相對或絕對路徑區段。

` *[!DNL catalogPath]*`是絕對或相對檔案路徑/名稱。 *[!DNL requestPath]*&#x200B;必須為相對檔案路徑/名稱。

可在[!DNL PlatformServer.conf]中定義多個`PS::staticContent.rootPaths`值。 如此一來，來源資料檔案便可以分散至多個檔案系統。 [!DNL Platform Server]會依指定的順序嘗試替代路徑，直到找到資料檔為止。
