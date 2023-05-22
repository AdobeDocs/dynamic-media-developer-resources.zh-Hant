---
title: 錯誤詳細資訊
description: 錯誤消息詳細資訊。 指定通過HTTP返回的錯誤消息的詳細級別，作為error.message值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---

# 錯誤詳細資訊{#errordetail}

錯誤消息詳細資訊。 指定通過HTTP返回的錯誤消息的詳細級別，作為error.message值。

## 標題 {#section-c10d75d72ee24d16a67cc8d927f1deba}

允許以下值：

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>僅標題。 返回錯誤的簡短一般說明。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>簡短留言。 保留供將來使用。 當前返回與0相同的資訊。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細消息。 提供有關錯誤的用戶級詳細資訊。 可能包括敏感資訊，如檔案路徑。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完全調試資訊。 在適用時添加Java™堆棧跟蹤。 錯誤影像從不包括堆棧跟蹤，而是返回2級資訊 <span class="codeph"> $error.message</span>。 </p></td> 
 </tr> 
</table>

* 建議對可公開訪問的活動伺服器使用0級。
* 建議將級別2用於暫存、質量保證和應用程式開發伺服器。
* 在向Dynamic Media技術支援報告問題時，第3級資訊可能很有用。

## 屬性 {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

枚舉值，必須為0、1、2或3。

## 預設 {#section-5e78d550050840cc9a1de811c581b94f}

繼承自 `default::ErrorDetail` 如果未指定或為空。

## 另請參閱 {#section-474e71922d194c7ca06f2aad3b30e025}

[屬性：:ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
