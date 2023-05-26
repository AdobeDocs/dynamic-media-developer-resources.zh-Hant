---
title: init
description: 全景檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# init{#init}

全景檢視器的JavaScript API參考。

`init()`

開始初始化「全景檢視器」。 此時，必須建立容器DOM元素，好讓檢視器程式碼可依其ID尋找它。

如果容器元素還不是網頁版面配置的一部分(例如，它可能使用以下專案隱藏： `display:none` 指定樣式)，檢視器會暫停其初始化程式。 直到網頁將容器元素帶回版面配置為止。 發生此事件時，檢視器會自動繼續載入。

在檢視器生命週期中只應呼叫一次此方法，後續呼叫會被忽略。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 檢視器例項的參考。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
