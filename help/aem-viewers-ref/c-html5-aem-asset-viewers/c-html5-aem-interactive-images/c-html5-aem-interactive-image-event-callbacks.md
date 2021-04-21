---
description: 事件回呼
solution: Experience Manager
title: 事件回呼
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner
exl-id: 59b8a88e-0139-4981-bfb9-f2dc1ac2337d
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---

# 事件回呼{#event-callbacks}

檢視器支援網頁用來追蹤檢視器初始化程式或執行時期行為的JavaScript事件回呼。

回呼處理常式是透過在檢視器的建構函式中，將具有`handlers`屬性的事件名稱和對應處理常式函式傳遞至`config` JSON物件來指派。 或者，也可使用`setHandlers()` API方法。

支援的檢視器事件包括：

<table id="table_D4A2035B65B140F882F550B711BD3160"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>檢視器事件 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> initComplete  </span> </p> </td> 
   <td colname="col2"> <p>在檢視器初始化完成並建立所有內部元件時觸發，如此便可使用<span class="codeph"> getComponent()</span> API。 回呼處理常式不會使用任何引數。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trackEvent  </span> </p> </td> 
   <td colname="col2"> <p> 每次在檢視器內發生事件時觸發，事件追蹤系統(例如Adobe Analytics)可處理該事件。 回呼處理常式接受下列引數： </p> <p> 
     <ul id="ul_8A5F409E32E94063AE8D3AB158A0E13D"> 
      <li id="li_1311D5DDD4454FBC9116BA8E2CB003B1"> <p> <span class="codeph"> objID {String}  </span> -目前未使用。 </p> </li> 
      <li id="li_C2ABD13097FA40A7B9801C0B7592FB59"> <p> <span class="codeph"> compClass {String}  </span> -目前未使用。 </p> </li> 
      <li id="li_3BE8001365714C3FAC32C9B2CFFD5DCE"> <p> <span class="codeph"> instName {String}  </span> -觸發事件的檢視器SDK元件的例項名稱。 </p> </li> 
      <li id="li_755DDE84B1CC4B4D8A3FA0C774CBA666"> <p> <span class="codeph"> timeStamp {Number}  </span> -事件時間戳記。 </p> </li> 
      <li id="li_05A1C45826AC4D1192CB72FE07EE4C29"> <p> <span class="codeph"> eventInfo {String}  </span> -事件裝載。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> quickViewActivate  </span> </p> </td> 
   <td colname="col2"> <p> 在用戶激活熱區時觸發，該熱區具有與其關聯的快速視圖資料。 回呼處理常式會採用下列引數： </p> <p> 
     <ul id="ul_171110934BD54839B371FAD8D2AD467B"> 
      <li id="li_7B14C3BA432B43E392AC103926807E88"> <p> <span class="codeph"> data {Object}  </span> -包含熱點定義中資料的JSON物件。欄位<span class="codeph"> sku </span>是必填欄位，而其他欄位則是選填欄位，並視來源熱點定義而定。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

另請參閱[InteractiveImage](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-interactiveimage.md#reference-bd16cadc0c054fafb0db4994741d47cd)和[setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)。
