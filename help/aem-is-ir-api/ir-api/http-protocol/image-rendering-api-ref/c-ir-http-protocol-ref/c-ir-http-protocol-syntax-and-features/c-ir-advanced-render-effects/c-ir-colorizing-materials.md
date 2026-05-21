---
title: 色彩化材質
description: 大多數材質都可動態上色。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
TQID: 'https://experienceleague.adobe.com/MGmuOj214tFPKeSGwz33pGn2m0B0fme1Cq-umlxG9v0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# 色彩化材質{#colorizing-materials}

大多數材質都可動態上色。

上色演演算法比較簡單，最適合色相範圍有限的材質影像。 若要將材質上色，轉譯器只會減去`bgc=`值，並將`color=`值加到每個畫素值。

如果未指定`color=`，則已停用色彩化。 封包材料會略過`bgc=`屬性；而是使用內嵌在[!DNL vnc]檔案中的基色值。
