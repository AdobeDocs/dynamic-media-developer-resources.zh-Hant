---
description: 錯誤訊息詳細資料。 指定透過HTTP傳回的錯誤訊息的詳細程度，作為error.message值。
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 5%

---

# ErrorDetail{#errordetail}

錯誤訊息詳細資料。 指定透過HTTP傳回的錯誤訊息的詳細程度，作為error.message值。

## 標題 {#section-c10d75d72ee24d16a67cc8d927f1deba}

允許下列值：

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>僅標題。 傳回錯誤的簡短一般說明。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>簡訊。 保留供將來使用。 目前傳回與0相同的資訊。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細訊息。 提供有關錯誤的用戶級詳細資訊。 可能包括敏感資訊，如檔案路徑。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完整的除錯資訊。 在適用時添加Java堆棧跟蹤。 錯誤影像從不包含堆棧跟蹤，而是在<span class="codeph"> $error.message</span>中返回級別2資訊。 </p></td> 
 </tr> 
</table>

* 建議將0級用於可公開存取的即時伺服器。
* 建議將2級用於測試、品質保證和應用程式開發伺服器。
* 在向Dynamic Media技術支援報告問題時，第3級資訊可能很有用。

## 屬性 {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

枚舉值必須為0、1、2或3。

## 預設 {#section-5e78d550050840cc9a1de811c581b94f}

如果未指定或為空，則從`default::ErrorDetail`繼承。

## 另請參閱 {#section-474e71922d194c7ca06f2aad3b30e025}

[屬性：:ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
