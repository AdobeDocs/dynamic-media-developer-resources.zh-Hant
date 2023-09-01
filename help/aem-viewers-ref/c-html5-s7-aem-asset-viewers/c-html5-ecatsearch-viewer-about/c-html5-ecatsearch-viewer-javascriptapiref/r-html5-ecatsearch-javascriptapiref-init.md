---
title: init
description: eCatalog檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# init{#init}

eCatalog檢視器的JavaScript API參考。

[!DNL `init()`]

啟動eCatalog檢視器的初始化。 此時，必須建立容器DOM元素，讓檢視器程式碼可依其ID尋找。

例如，如果容器元素還不是網頁版面配置的一部分，則它可能會使用以下專案隱藏 [!DNL `display:none`] 指定給檢視器的樣式 — 檢視器會暫停其初始化程式。 直到網頁將容器元素帶回版面配置為止。 發生此事件時，檢視器會自動繼續載入。

在檢視器生命週期中僅呼叫此方法一次；後續呼叫會被忽略。

## 參數 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

無。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] 檢視器例項的參考。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
