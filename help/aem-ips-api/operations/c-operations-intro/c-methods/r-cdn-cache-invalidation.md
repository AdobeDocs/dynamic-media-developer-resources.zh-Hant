---
description: 將提供的URL清單轉送至Dynamic Media CDN（內容分送網路）提供者，使其現有的HTTP回應快取失效。
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 65b758f2-b49a-4616-b657-a64808c9202a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 4%

---

# cdnCacheInvalidation{#cdncacheinvalidation}

將提供的URL清單轉送至Dynamic Media CDN（內容分送網路）提供者，使其現有的HTTP回應快取失效。

## cdnCacheInvalidation:關於 {#section-4f70d2bc79d64288b961836ab17e9690}

CDN快取失效會強制這些URL的所有HTTP請求，在透過CDN網路處理此無效請求後，就會根據Dynamic Media網路上目前發佈的資料重新驗證。 任何未連線至Dynamic Media服務URL結構且在建立公司時直接符合指派給Dynamic Media公司的根ID的URL，都會導致整個請求的API錯誤。 任何CDN不支援且認為無效的URL，也會導致整個請求的API錯誤。

**使用頻率：規則**

Dynamic Media的CDN合作夥伴可控制使用此功能頻率的規則。 CDN仍可自行決定降低這些無效判定的回應速度，以維持其服務對使用者的最佳效能。 如果Dynamic Media收到過度使用此功能的通知，我們需要針對每個公司或整個服務使用停用此功能。

**確認電子郵件**

Dynamic Media CDN合作夥伴的確認電子郵件可傳送給清單的建立者，或最多5個其他電子郵件地址。 當通知整個CDN網路已清除電子郵件中參考的URL時，API會傳送確認。 如果提供的URL數量超過Dynamic Media可在單一通知上傳送給CDN合作夥伴的數量，則對`cdnCacheInvalidation`的單一呼叫可傳送多封電子郵件。 目前則是當請求超過100個URL時，但可能會根據CDN合作夥伴的請求而有所變更。

**支援時間**

6.0

## 授權的使用者類型 {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## 參數 {#section-bd1ed2b7419945d19a2ebd5668499f72}

**輸入** ( `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 名稱</b> </th> 
   <th class="entry"> <b> 類型</b> </th> 
   <th class="entry"> <b> 必要</b> </th> 
   <th class="entry"> <b> 說明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> 是 </p> </td> 
   <td> <p> 與URL連結之公司的控制代碼，要使其失效。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 類型：UrlArray</span> </p> </td> 
   <td> <p> 是 </p> </td> 
   <td> <p> 從CDN快取失效的最多1000個URL清單。 所有URL都必須包含要失效的Dynamic Media公司根ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出**( `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 名稱</b> </th> 
   <th class="entry"> <b> 類型</b> </th> 
   <th class="entry"> <b> 必要</b> </th> 
   <th class="entry"> <b> 說明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>引用清除請求的句柄。 </p> <p><span class="codeph"> cdnCacheInvalidation</span> API現在幾乎立即讓快取失效（~5秒）。 因此，無效狀態的輪詢通常不再需要。 </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>完成清除請求的估計秒數。 用戶端應等待此時間再進行輪詢狀態。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-f414361a58e84dfcbbac30a358d02125}

此範例會要求CDN快取中的四個URL失效。 回應包含作業成功的摘要計數，以及直接從CDN提供的錯誤詳細資訊清單，以協助用戶端使用此功能。

`getCdnCacheInvalidationStatus` 作業.

**請求**

```java
<cdnCacheInvalidationParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <companyHandle>c|6</companyHandle>
   <urlArray>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$thumbnail$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$product$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$large$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/ImageSetConfigDefaults?req=userdata</items>
    </urlArray>
</cdnCacheInvalidationParam>
```

**回答**

```java
<cdnCacheInvalidationReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</cdnCacheInvalidationReturn>
```
