---
description: 「影像伺服」來源資料檔案包含影像和遮色片檔案、字型和ICC設定檔。
solution: Experience Manager
title: Source資料
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
TQID: 'https://experienceleague.adobe.com/36EvEOjHZ8ik-gps-vaap5PhFCf5rwV9ecfkKHZcIhk'
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
source-wordcount: 190
ht-degree: 0%

---

# Source資料{#source-data}

「影像伺服」來源資料檔案包含影像和遮色片檔案、字型和ICC設定檔。

影像伺服器必須能夠存取所有來源資料檔案。 「影像伺服」提供許多指定資料檔案位置的替代方式：

`*`install_folder`*/ *`rootPath`*/ *`filePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS：：RootPath/attribute：：RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">檔案路徑</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">目錄路徑</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">目錄：：Path|目錄：：MaskPath|icc：：ProfilePath|font：：FontPath|font：：MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p>在「影像伺服」HTTP要求中指定的<span class="codeph">相對影像檔案路徑和名稱</span> </p></td> 
 </tr> 
</table>

伺服器會由右至左組合路徑區段，直到建立絕對檔案路徑為止。

所有`*`rootPath`*`區段都可以是空白、相對或絕對路徑區段。

`*`catalogPath`*`是絕對或相對檔案路徑/名稱。 `*`requestPath`*`必須為相對檔案路徑/名稱。

`Multiple IS::RootPath`值可以在ImageServerRegistry.xml中定義（或透過管理介面）。 如此一來，來源資料檔案便可以分散至多個檔案系統。 影像伺服器會依指定的順序嘗試替代路徑，直到找到資料檔案為止。

任何型別的新資料檔案都可以隨時新增，不需要停止伺服器。
