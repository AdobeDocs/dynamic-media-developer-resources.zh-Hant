---
description: 影像伺服器proxy可用來調整日文手機影像大小。
solution: Experience Manager
title: 影像伺服器Proxy
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---


# 影像伺服器proxy{#image-server-proxy}

影像伺服器proxy可用來調整日文手機影像大小。

## URL 格式 {#section-2e8c40b0547c4f99874cdf502b338940}

IS Proxy的URL格式與一般的IS要求非常類似。 傳遞至proxy的任何IS修飾元都會傳遞至影像伺服器。 您可以在[HTTP通訊協定參考](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e)中找到IS修飾元的資訊。

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## 特定於代理的修飾詞清單{#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定要用作影像寬度的設備可用寬度的百分比。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 平均百分比=  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定裝置可用高度的百分比，以用作影像高度。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 大小百分比=  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定設備的「記憶體限制嵌入式介質」屬性的百分比，以將響應大小限制為。 這僅適用於jpg回應。 影像品質會降低，直到回應大小在指定百分比內為止。 </p></td> 
 </tr> 
</table>

## 內嵌影像記憶體限制{#section-52f7c69ed8a341ceabf92ceee19b0f36}

如果裝置對可內嵌在網頁上的影像大小有限制，只要回應格式為jpg，影像大小就會限制在該大小。 如果裝置沒有任何限制，則代理會將回應限制為500MB。

## 後端處理{#section-bdf7c294b6824de9969c97fc1f8aa6d3}

Proxy會每天下載、驗證及載入Device Atlas資料檔案一次。 驗證會提取不同裝置的不同屬性，並在接受新資料前將其與預期值進行比較。
