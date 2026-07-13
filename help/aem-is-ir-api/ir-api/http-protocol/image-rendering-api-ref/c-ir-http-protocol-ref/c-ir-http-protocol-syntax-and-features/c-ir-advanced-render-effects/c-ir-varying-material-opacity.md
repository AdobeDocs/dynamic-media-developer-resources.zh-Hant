---
title: 不同材質不透明度
description: 實色和套用至重疊物件的可重複紋理，以及貼花和視窗遮蓋材料都支援可變不透明度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
TQID: 'https://experienceleague.adobe.com/i4d6vy62vn9BfFrS2W0srO671N9Ad4hCUXR7J4cajJA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 0%

---

# 不同材質不透明度{#varying-material-opacity}

實色和套用至重疊物件的可重複紋理，以及貼花和視窗遮蓋材料都支援可變不透明度。

只需搭配使用RGB影像與Alpha色版，即可提供不透明度資訊。 此外，整體不透明度可以用`opacity=`命令改變（RGB和RGBA影像皆可）。

壁框線也支援RGBA影像，主要是為了支援壓鑄模裁切的框線。

定義視窗涵蓋範圍的[!DNL vnw]檔案可以包含不透明度通道。 它由轉譯器與可重複紋理的Alpha色版和`opacity=`值結合，以提供各種透明效果，用於透明和半透明視窗處理。

