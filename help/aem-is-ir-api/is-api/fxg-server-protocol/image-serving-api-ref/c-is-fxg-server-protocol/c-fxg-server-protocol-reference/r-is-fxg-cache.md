---
description: 快取控制。 允許選擇性地停用內部平台伺服器快取中的用戶端快取（瀏覽器、代理伺服器、網路快取系統）和快取。
solution: Experience Manager
title: 快取
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# cache{#cache}

快取控制。 允許選擇性地停用內部平台伺服器快取中的用戶端快取（瀏覽器、代理伺服器、網路快取系統）和快取。

`&cache= *`cacheControl`*`

`&cache= *`clientControlserverControl`*, *``*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 開啟／關閉</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 開啟／關閉</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 開啟／關閉</span> </p></td> 
 </tr> 
</table>

如果只指定一個&#x200B;*`cacheControl`*&#x200B;值，則它將同時應用於客戶機和伺服器快取。

請求屬性。 當請求未傳回回回覆影像時忽略。 *`clientControl`* 會在影像目錄停用用戶端快取時忽略(如果 `catalog::Expiration` 有負值)。

預設為`cache=on,on`。
