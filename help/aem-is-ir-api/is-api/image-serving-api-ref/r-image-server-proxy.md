---
description: 可以使用影像伺服器代理來調整日本電話的影像大小。
solution: Experience Manager
title: 映像伺服器代理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# 映像伺服器代理{#image-server-proxy}

可以使用影像伺服器代理來調整日本電話的影像大小。

## URL 格式 {#section-2e8c40b0547c4f99874cdf502b338940}

IS代理的URL格式與常規IS請求非常相似。 傳遞給代理的任何IS修改符都會傳遞給映像伺服器。 可在 [HTTP協定引用](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e)。

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## 代理特定修改量清單 {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widperct = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定要用作影像寬度的設備可用寬度的百分比。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 海百分比= &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定要用作影像高度的設備可用高度的百分比。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 大小百分比= &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定設備的「記憶體限制嵌入媒體」屬性的百分比，以將響應大小限制為。 這僅適用於jpg響應。 在響應大小在指定百分比內之前，會降低影像質量。 </p></td> 
 </tr> 
</table>

## 嵌入式影像儲存器限制 {#section-52f7c69ed8a341ceabf92ceee19b0f36}

如果設備對可嵌入到網頁上的影像大小有限制，則只要響應格式為jpg，影像大小就限制為該大小。 如果設備沒有任何限制，則代理將響應限制為500MB。

## 後端處理 {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

代理每天下載、驗證和載入Device Atlas資料檔案一次。 該驗證將不同設備的不同屬性拔出，並在接受新資料之前將其與預期值進行比較。
