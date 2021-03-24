---
description: 錯誤消息詳細資訊。 指定透過HTTP傳回之錯誤訊息的詳細程度，作為error.message值。
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 5%

---


# ErrorDetail{#errordetail}

錯誤消息詳細資訊。 指定透過HTTP傳回之錯誤訊息的詳細程度，作為error.message值。

## 標題 {#section-c10d75d72ee24d16a67cc8d927f1deba}

允許使用下列值：

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>僅限標題。 傳回錯誤的簡短一般說明。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>簡短訊息。 留待日後使用。 目前傳回與0相同的資訊。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細訊息。 提供有關錯誤的用戶級詳細資訊。 可能包含敏感資訊，例如檔案路徑。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完整的除錯資訊。 添加Java堆棧跟蹤（如果適用）。 錯誤影像從不包含堆疊追蹤，而是傳回<span class="codeph"> $error.message</span>中的2級資訊。 </p></td> 
 </tr> 
</table>

* 建議對可公開存取的即時伺服器使用0級。
* 建議使用2級來測試、品質保證和應用程式開發伺服器。
* 在向Dynamic Media技術支援報告問題時，第3級資訊可能很有用。

## 屬性 {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

列舉值必須為0、1、2或3。

## 預設 {#section-5e78d550050840cc9a1de811c581b94f}

如果未指定或為空，則繼承自`default::ErrorDetail`。

## 另請參閱 {#section-474e71922d194c7ca06f2aad3b30e025}

[屬性：:ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
