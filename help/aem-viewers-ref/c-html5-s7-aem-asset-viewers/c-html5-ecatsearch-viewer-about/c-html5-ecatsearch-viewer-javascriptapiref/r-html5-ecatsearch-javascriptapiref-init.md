---
title: init
description: eCatalog檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
TQID: 'https://experienceleague.adobe.com/Hb-C6aORHF8--oX3IqgRZIi1rfbLg39F0Ewzb4sg45U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 2%

---

# init{#init}

eCatalog檢視器的JavaScript API參考。

[!DNL `init()`]

啟動eCatalog檢視器的初始化。 此時，必須建立容器DOM元素，讓檢視器程式碼可依其ID尋找。

如果容器元素尚未成為網頁版面配置的一部分（例如，可能使用指派給它的[!DNL `display:none`]樣式將其隱藏），檢視器會暫停其初始化程式。 直到網頁將容器元素帶回版面配置為止。 發生此事件時，檢視器會自動繼續載入。

在檢視器生命週期中僅呼叫此方法一次；後續呼叫會被忽略。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`]檢視器執行個體的參考。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
