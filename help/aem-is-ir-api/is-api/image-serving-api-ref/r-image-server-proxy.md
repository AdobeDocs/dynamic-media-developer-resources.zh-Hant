---
description: 影像伺服器代理可用於調整日文電話的影像大小。
solution: Experience Manager
title: 影像伺服器代理
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# 影像伺服器代理{#image-server-proxy}

影像伺服器代理可用於調整日文電話的影像大小。

## URL 格式 {#section-2e8c40b0547c4f99874cdf502b338940}

IS Proxy的url格式與一般IS要求非常類似。 傳遞至代理的任何IS修飾元都會傳遞至影像伺服器。 您可以在[HTTP通訊協定參考](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e)中找到IS修飾元的相關資訊。

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## 代理特定修飾符清單 {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定要用作影像寬度的設備可用寬度的百分比。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 平等=  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定要用作影像高度的設備可用高度的百分比。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 大小百分比=  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定設備的「記憶體限制嵌入式介質」屬性的百分比，以將響應大小限制為。 這僅適用於jpg回應。 影像品質會降低，直到回應大小在指定百分比內為止。 </p></td> 
 </tr> 
</table>

## 嵌入式影像儲存器限制 {#section-52f7c69ed8a341ceabf92ceee19b0f36}

如果裝置對可內嵌在網頁上的影像大小有限制，只要回應格式為jpg，影像大小就會限制為該大小。 如果裝置沒有任何限制，則代理將回應限制為500MB。

## 後端處理 {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

代理每天下載、驗證和載入Device Atlas資料檔案一次。 驗證會針對不同裝置提取不同屬性，並在接受新資料前與預期值比較。
