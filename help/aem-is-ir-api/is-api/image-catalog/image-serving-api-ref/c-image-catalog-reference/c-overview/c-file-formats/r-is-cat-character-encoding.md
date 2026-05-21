---
description: 「影像伺服」支援採用ISO-8859-1和UTF-8編碼的影像目錄。
solution: Experience Manager
title: 字元編碼
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
TQID: 'https://experienceleague.adobe.com/tsIJu-zCT-NlV6SD1I1pPYQ0DfqNcu9jSCBVXCcQ9tE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# 字元編碼{#character-encoding}

「影像伺服」支援採用ISO-8859-1和UTF-8編碼的影像目錄。

位元組順序標籤(BOM)可用來指定每個檔案的編碼。 對於UTF-8，BOM是位元組序列`EF BB BF`。 在每個影像目錄檔案的開頭偵測到此字元序列時，會採用UTF-8編碼。 任何其他位元組序列都會將檔案解譯成ISO-8859-1標準。

許多當代應用程式在針對UTF-8進行配置時，會自動插入BOM。
