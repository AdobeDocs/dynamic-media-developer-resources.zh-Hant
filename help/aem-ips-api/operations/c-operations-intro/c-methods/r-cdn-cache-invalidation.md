---
description: 將提供的URL清單轉送至Dynamic Media CDN （內容發佈網路）提供者，以使其現有的HTTP回應快取失效。
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 65b758f2-b49a-4616-b657-a64808c9202a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 1%

---

# cdnCacheInvalidation{#cdncacheinvalidation}

將提供的URL清單轉送至Dynamic Media CDN （內容發佈網路）提供者，以使其現有的HTTP回應快取失效。

## cdnCacheInvalidation：關於 {#section-4f70d2bc79d64288b961836ab17e9690}

CDN快取失效會強制在透過CDN網路處理此失效請求後，根據動態媒體網路上的目前發佈資料，重新驗證這些URL的所有HTTP請求。 未連線至Dynamic Media服務URL結構且直接比對公司建立時指派之Dynamic Media公司根ID的任何URL，都會導致整個請求的API錯誤。 CDN不支援且視為無效的任何無效URL也會導致整個請求的API錯誤。

**使用頻率：規則**

控管此功能使用頻率的規則由Dynamic Media的CDN合作夥伴控制。 CDN保留降級這些無效回應能力的酌情權，以維持其為使用者提供的最佳服務效能。 如果Dynamic Media收到過度使用此功能的通知，Adobe必須根據每個公司或整個服務來停用此功能。

**確認電子郵件**

來自Dynamic Media CDN合作夥伴的確認電子郵件可以傳送給清單的建立者或最多5個其他電子郵件地址。 當通知整個CDN網路電子郵件中參照的URL已清除時，API會傳送確認。 如果提供的URL數目超過Dynamic Media在單一通知上可傳送給CDN合作夥伴的數目，則對`cdnCacheInvalidation`的單一呼叫可傳送多封電子郵件。 目前這表示要求超過100個URL，但可能根據CDN合作夥伴的要求而有所變更。

**自**&#x200B;起便支援

6.0

## 授權的使用者型別 {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## 參數 {#section-bd1ed2b7419945d19a2ebd5668499f72}

**輸入** ( `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>名稱</b> </th> 
   <th class="entry"> <b>型別</b> </th> 
   <th class="entry"> 需要<b></b> </th> 
   <th class="entry"> <b>描述</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd：string</span> </p> </td> 
   <td> <p> 是 </p> </td> 
   <td> <p> 與要失效的URL連結的公司控制代碼。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph">型別：UrlArray</span> </p> </td> 
   <td> <p> 是 </p> </td> 
   <td> <p> 要從CDN快取中失效的1000個URL清單。 所有URL都必須包含要失效的Dynamic Media公司根ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出**( `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>名稱</b> </th> 
   <th class="entry"> <b>型別</b> </th> 
   <th class="entry"> 需要<b></b> </th> 
   <th class="entry"> <b>描述</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>參照清除請求的控點。 </p> <p><span class="codeph"> cdnCacheInvalidation</span> API現在幾乎立即讓快取失效（~5秒）。 因此，通常不再需要輪詢失效狀態。 </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：int</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>預計完成清除要求的秒數。 使用者端應等待此時間，再輪詢狀態。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-f414361a58e84dfcbbac30a358d02125}

此範例要求在CDN快取中讓四個URL失效。 回應包含操作成功的摘要計數，以及直接從CDN提供的錯誤詳細資訊清單，以協助使用者端使用此功能。

`getCdnCacheInvalidationStatus`作業。

**要求**

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

**回應**

```java
<cdnCacheInvalidationReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</cdnCacheInvalidationReturn>
```
