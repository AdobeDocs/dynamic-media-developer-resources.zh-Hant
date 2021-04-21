---
description: 將提供的URL清單轉送至Dynamic MediaCDN（內容散發網路）提供者，使其現有的HTTP回應快取無效。
solution: Experience Manager
title: cdnCacheInvaliting
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 4%

---


# cdnCacheInvalidation{#cdncacheinvalidation}

將提供的URL清單轉送至Dynamic MediaCDN（內容散發網路）提供者，使其現有的HTTP回應快取無效。

## cdnCacheInvalidation:關於{#section-4f70d2bc79d64288b961836ab17e9690}

CDN快取失效會強制這些URL的所有HTTP要求，在此失效要求透過CDN網路處理後，針對Dynamic Media網路上目前發佈的資料重新驗證。 任何未連線至Dynamic Media服務URL結構且與建立公司時指派的Dynamic Media公司根ID直接相符的URL，都會導致整個請求發生API錯誤。 CDN不支援且認為無效的任何無效URL，也會導致整個請求的API錯誤。

**使用頻率：規則**

控制此功能使用頻率的規則由Dynamic Media的CDN合作夥伴控制。 CDN保留降低這些無效回應的酌情權，以維持其服務對其使用者的最佳效能。 如果Dynamic Media收到過度使用此功能的通知，我們必須針對每個公司或整個服務禁用此功能。

**確認電子郵件**

來自Dynamic MediaCDN合作夥伴的確認電子郵件可傳送至清單的建立者，或最多5個其他電子郵件地址。 當通知整個CDN網路已清除電子郵件中參考的URL時，API會傳送確認。 如果提供的URL數量超過Dynamic Media在單一通知上可傳送給CDN合作夥伴的數量，則單一呼叫`cdnCacheInvalidation`可傳送多封電子郵件。 目前，這是當要求超過100個URL時，但可能會根據CDN合作夥伴的要求而變更。

**支援自**

6.0

## 授權用戶類型{#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## 參數 {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Input** ( `cdnCacheInvalidationParam`)

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
   <td> <p> 與URL連接的公司的控制代碼無效。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 類型：UrlArray</span> </p> </td> 
   <td> <p> 是 </p> </td> 
   <td> <p> 從CDN快取中失效的URL清單最多達1000個。 所有URL都必須包含要失效的Dynamic Media公司根ID。 </p> </td> 
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
   <td colname="col4"> <p>引用清除請求的句柄。 </p> <p><span class="codeph"> cdnCacheInvaliting</span> API現在幾乎立即使快取失效（~5秒）。 因此，通常不再需要輪詢失效狀態。 </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 估計秒數</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>完成清除請求的預計秒數。 客戶端應等待此時間，才能輪詢狀態。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-f414361a58e84dfcbbac30a358d02125}

此範例要求在CDN快取中使四個URL無效。 回應包含操作成功的摘要計數和直接從CDN提供的錯誤詳細資料清單，以協助用戶端使用此功能。

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

