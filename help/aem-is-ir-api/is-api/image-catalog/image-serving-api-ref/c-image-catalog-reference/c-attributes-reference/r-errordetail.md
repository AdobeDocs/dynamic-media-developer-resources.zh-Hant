---
description: 錯誤消息詳細資訊。 指定通過HTTP返回的錯誤消息的詳細級別，作為error.message值。
solution: Experience Manager
title: 錯誤詳細資訊
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 4%

---

# 錯誤詳細資訊{#errordetail}

錯誤消息詳細資訊。 指定通過HTTP返回的錯誤消息的詳細級別，作為error.message值。

允許以下值：

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>僅標題。 返回錯誤的簡短一般說明。 建議用於可以公開訪問的即時伺服器。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>簡短留言。 保留供將來使用。 當前返回與0相同的資訊。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>詳細消息。 提供有關錯誤的用戶級詳細資訊。 可能包括敏感資訊，如檔案路徑。 建議使用暫存、質量保證和應用程式開發伺服器。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完全調試資訊。 在適用時添加Java堆棧跟蹤。 錯誤影像從不包括堆棧跟蹤，而是返回2級資訊 <span class="codeph"> $error.message</span>。 在向Dynamic Media技術支援報告問題時，這些資訊可能非常有用。 </p></td> 
 </tr> 
</table>

## 屬性 {#section-e167895723ca4ad4ba283d3d7b4324de}

枚舉值，必須為0、1、2或3。

## 預設 {#section-8f27098e509945a18676aca0675c8f41}

繼承自 `default::ErrorDetail` 如果未指定或為空。

## 另請參閱 {#section-5451b0525ed74121950bfc34726c3970}

[屬性：:ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
