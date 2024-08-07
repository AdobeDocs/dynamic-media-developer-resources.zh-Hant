---
description: 錯誤訊息詳細資料。 指定透過HTTP傳回之錯誤訊息的詳細資訊層級為error.message值。
solution: Experience Manager
title: 錯誤詳細資料
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 4%

---

# 錯誤詳細資料{#errordetail}

錯誤訊息詳細資料。 指定透過HTTP傳回之錯誤訊息的詳細資訊層級為error.message值。

允許的值如下：

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>僅限標題。 傳回錯誤的簡短一般說明。 建議可供公開存取的即時伺服器使用。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>簡短訊息。 保留以供日後使用。 目前傳回的資訊與0相同。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細訊息。 提供有關錯誤的使用者層級詳細資訊。 可能包含敏感資訊，例如檔案路徑。 建議用於中繼、品質保證和應用程式開發伺服器。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完整的偵錯資訊。 新增Java棧疊追蹤（如適用）。 錯誤影像絕不包含棧疊追蹤，而是在<span class="codeph"> $error.message</span>中傳回層級2資訊。 向Dynamic Media技術支援報告問題時，此資訊會很有用。 </p></td> 
 </tr> 
</table>

## 屬性 {#section-e167895723ca4ad4ba283d3d7b4324de}

列舉值，必須是0、1、2或3。

## 預設 {#section-8f27098e509945a18676aca0675c8f41}

如果未指定或空白，則繼承自`default::ErrorDetail`。

## 另請參閱 {#section-5451b0525ed74121950bfc34726c3970}

[attribute：：ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
