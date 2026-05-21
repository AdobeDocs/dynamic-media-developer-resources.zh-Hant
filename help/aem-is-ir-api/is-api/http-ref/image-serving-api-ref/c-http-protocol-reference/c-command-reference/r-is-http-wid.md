---
title: wid
description: 檢視寬度。 指定請求中不存在fit=時回應影像（檢視影像）的寬度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
TQID: 'https://experienceleague.adobe.com/n6U4pPJuxOo3rX2nU7EYsnevrCPBzoYq5SiQvrr5t20'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 274
ht-degree: 1%

---

# wid{#wid}

檢視寬度。 指定請求中不存在fit=時回應影像（檢視影像）的寬度。

`wid= *`值`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">值</span> </p> </td> 
  <td class="stentry"> <p>影像寬度，以畫素為單位（int大於0）。 </p> </td> 
 </tr> 
</table>

如果同時指定`hei=`和`scl=`，則可根據`align=`屬性裁切複合影像。 當`fit=`出現時，`wid=`會指定精確、最小或最大回應影像寬度；如需詳細資料，請參閱`fit=`的說明。

如果未指定`scl=`，則會縮放複合影像以符合大小。 如果同時指定`wid=`和`hei=`，但未指定`scl=`，則會縮放影像以完全符合wid/hei矩形，儘可能留下最小的背景區域。 在此情況下，影像會根據`align=`屬性放置在檢視矩形內。

>[!NOTE]
>
>如果計算的或預設的回覆影像大小大於`attribute::MaxPix`，則會傳回錯誤。

## 預設 {#section-976d4c8554a34c899f85d172f6ac6f58}

若未指定`wid=`、`hei=`或`scl=`，則回覆影像的大小可能為複合影像或`attribute::DefaultPix` （取較小者）。

## 屬性 {#section-c93b7ce1b0d2475f80b06264b45d1285}

檢視屬性。 無論目前的圖層設定為何，都適用。

## 範例 {#section-82bc98b7c15a451bbe9b915d414c0470}

要求影像以便能放入200x200矩形中；如果影像不是正方形，則由右上角對齊。 任何背景區域已填滿`attribute::BkgColor`。

` http:// *`伺服器`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

相同的影像，以200畫素的固定寬度傳送，但具有可變高度以維持影像的外觀比例。 在此情況下，傳回的影像絕對不會有任何背景填滿區域。 在這種情況下，`align=`完全沒有效果。

` http:// *`伺服器`*/myRootId/myImageId?wid=200`

## 另請參閱 {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) ， [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)， [attribute：：DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)， [attribute：：MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
