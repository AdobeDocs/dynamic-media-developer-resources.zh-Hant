---
description: 錯誤消息詳細資訊。 指定透過HTTP傳回之錯誤訊息的詳細程度，作為error.message值。
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 4%

---


# ErrorDetail{#errordetail}

錯誤消息詳細資訊。 指定透過HTTP傳回之錯誤訊息的詳細程度，作為error.message值。

允許使用下列值：

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>僅限標題。 傳回錯誤的簡短一般說明。 建議用於可公開存取的即時伺服器。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>簡短訊息。 留待日後使用。 目前傳回與0相同的資訊。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細訊息。 提供有關錯誤的用戶級詳細資訊。 可能包含敏感資訊，例如檔案路徑。 建議用於測試、品質保證和應用程式開發伺服器。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完整的除錯資訊。 添加Java堆棧跟蹤（如果適用）。 錯誤影像從不包含堆疊追蹤，而是傳回<span class="codeph"> $error.message</span>中的2級資訊。 在向Dynamic Media技術支助部門報告問題時，這些資訊可以派上用場。 </p></td> 
 </tr> 
</table>

## 屬性 {#section-e167895723ca4ad4ba283d3d7b4324de}

列舉值必須為0、1、2或3。

## 預設 {#section-8f27098e509945a18676aca0675c8f41}

如果未指定或為空，則繼承自`default::ErrorDetail`。

## 另請參閱 {#section-5451b0525ed74121950bfc34726c3970}

[屬性：:ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
