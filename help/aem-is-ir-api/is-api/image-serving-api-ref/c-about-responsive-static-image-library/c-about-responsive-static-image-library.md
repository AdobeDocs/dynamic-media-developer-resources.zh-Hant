---
description: 響應影像庫是JavaScript模組，可動態調整從Dynamic Media提供並嵌入響應網頁的影像的質量。 此外，它在具有高密度螢幕的器件上提供了改進的影像質量。 庫還可以響應性地渲染來自Smart Crop和Smart Swatch的結果。
solution: Experience Manager
title: 關於響應映像庫
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# 關於響應映像庫{#about-responsive-image-library}

響應影像庫是JavaScript模組，可動態調整從Dynamic Media提供並嵌入響應網頁的影像的質量。 此外，它在具有高密度螢幕的器件上提供了改進的影像質量。 庫還可以響應性地渲染來自Smart Crop和Smart Swatch的結果。

## 演示URL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

響應影像庫的最簡單使用情形是定義影像寬度的斷點值清單。 此清單確保當由於用戶調整瀏覽器窗口大小或更改設備方向而改變網頁佈局而調整影像大小時載入和顯示適當的格式副本。 該庫在螢幕上連續監視影像大小，並且每次到達新的斷點寬度時，它都會從Dynamic Media獲取新的影像格式副本。

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>演示URL </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>下面是一個簡單示例，其中響應影像位於佔網頁寬度50%的容器內。 每次調整瀏覽器窗口大小時，容器寬度都會變化。 當影像寬度達到配置的斷點之一時，下載並顯示新格式副本。 目的是避免載入不必要的大映像，節省網路頻寬。 </p> <p>按一下URL以開啟網頁、調整瀏覽器窗口大小和監控網路流量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>以下Bootstrap示例說明了網頁中的相同用例。 根據BootstrapCSS，添加響應影像的佈局單元可以具有以下寬度之一：360、720和940像素。 這些值正是作為斷點傳遞給響應影像庫的值。 因此，Dynamic Media確保客戶端的網路頻寬得到有效利用。 此外，它還確保以給定當前網頁佈局所需的精確大小顯示影像，而不會因縮放客戶端瀏覽器而產生任何視覺偽像。 </p> <p>按一下URL以開啟網頁、調整瀏覽器窗口大小以達到不同的佈局斷點並監控網路流量。 </p> <p>更高級的使用案例包括將不同的「影像預設」或「影像服務」命令或兩者與不同的斷點值相關聯。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html</a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>在下一個示例中，使用不同影像質量和格式的不同斷點大小的影像預設。 對於小斷點，應用低質量預設，該預設強制「影像服務」返回僅壓縮為六色的GIF影像。 中斷點使用配置為高JPEG的影像預設。 最大斷點與使用無損PNG的高質量影像預設相關聯。 這種方法基於具有較大螢幕的設備具有更大的頻寬和處理能力的假設，確保高質量影像被遞送到這種設備。 </p> <p>按一下URL以開啟網頁，將Web瀏覽器窗口從大到小調整大小，並注意影像質量的降低。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>除了「影像預設」之外，還可以將特定的「影像服務」命令與斷點相關聯。 以下示例說明如何隨著螢幕影像大小變小而逐漸將標題影像裁剪到感興趣區域。 此處，最大斷點根本沒有任何Image Serving命令，因此標題影像是完全可見的。 在中斷點處應用中間裁剪，僅使文本為「正在運行」的運行程式可見。 在小斷點處，應用更多裁剪，以便只顯示產品。 </p> <p>按一下URL，開啟網頁並調整瀏覽器窗口的大小。 注意影像在從大到小的過程中如何逐漸收縮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>還可以將「影像服務」命令與「影像服務模板」一起使用，以根據影像大小控制某些模板參數。 在下一個示例中，使用影像服務模板，其中文本覆蓋的字型大小使用參數化 <span class="codeph"> $fontsize </span> 的下界。 響應影像配置為使用較大字型大小來減小影像大小，以確保文本始終保持可讀性： </p> </td> 
  </tr> 
 </tbody> 
</table>

## 系統需求 {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**伺服器硬體和軟體**

* Dynamic Media影像服6.0.1或更高版本。

**客戶端瀏覽器最低要求**

* Microsoft® Windows® 7或更高版本；macOSX 10.8或更高版本。
* Firefox 23、Safari 6、Chrome 29、IE 9或更高版本。
* iOS6號或更高版本。
* 已在iPhone3GS或更高版本和iPad2或更高版本（僅限本機瀏覽器）上認證。
* Android™ OS 2.3或更高版本。
* 當前不支援移動設備上的Internet Explorer。
