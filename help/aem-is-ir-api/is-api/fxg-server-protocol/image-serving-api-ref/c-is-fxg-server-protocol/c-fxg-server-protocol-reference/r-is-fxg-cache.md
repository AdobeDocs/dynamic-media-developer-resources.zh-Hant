---
description: 快取控制。 允許有選擇地禁用內部中的客戶端快取（瀏覽器、代理伺服器、網路快取系統）和快取 [!DNL Platform Server] 快取。
solution: Experience Manager
title: 快取
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# 快取{#cache}

快取控制。 允許有選擇地禁用內部中的客戶端快取（瀏覽器、代理伺服器、網路快取系統）和快取 [!DNL Platform Server] 快取。

`&cache= *`快取控制`*`

`&cache= *`客戶端控制項`*, *`伺服器控制`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 快取控制</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 關</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 客戶端控制項</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 關</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 伺服器控制</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 關</span> </p></td> 
 </tr> 
</table>

如果只有一個 *`cacheControl`* 值已指定，它應用於客戶端和伺服器快取。

請求屬性。 當請求未返回回復影像時忽略。 *`clientControl`* 當映像目錄禁用客戶端快取時忽略(如果 `catalog::Expiration` 為負值)。

預設為 `cache=on,on`。
