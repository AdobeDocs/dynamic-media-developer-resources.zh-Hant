---
description: 快取控制。 允許選擇性地停用內部平台伺服器快取中的用戶端快取（瀏覽器、代理伺服器、網路快取系統）和快取。
seo-description: 快取控制。 允許選擇性地停用內部平台伺服器快取中的用戶端快取（瀏覽器、代理伺服器、網路快取系統）和快取。
seo-title: 快取
solution: Experience Manager
title: 快取
topic: Scene7 Image Serving - Image Rendering API
uuid: 10332f0d-4ed3-4981-8034-46dffa5d68b0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
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
