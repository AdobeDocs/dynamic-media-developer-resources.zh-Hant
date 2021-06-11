---
description: 回應式影像庫是JavaScript模組，可動態調整從Dynamic Media提供並內嵌至回應式網頁的影像品質。 此外，在具有高密度螢幕的裝置上，它還可改善影像品質。 程式庫也可回應性地從智慧型裁切和智慧型色票轉譯結果。
solution: Experience Manager
title: 關於回應式影像庫
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 417fd2540c15762356dfb60aa7eb635ee5f74d13
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 0%

---

# 關於回應式影像庫{#about-responsive-image-library}

回應式影像庫是JavaScript模組，可動態調整從Dynamic Media提供並內嵌至回應式網頁的影像品質。 此外，在具有高密度螢幕的裝置上，它還可改善影像品質。 程式庫也可回應性地從智慧型裁切和智慧型色票轉譯結果。

## 示範URL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

回應式影像庫最簡單的使用案例是定義影像寬度的斷點值清單。 此清單可確保在調整影像大小時載入並顯示適當的轉譯，因為網頁版面會從調整瀏覽器視窗大小或變更裝置方向的使用者變更而改變。 程式庫會持續監控螢幕影像大小，每當達到新的斷點寬度時，就會從Dynamic Media擷取新的影像轉譯。

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>示範URL </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html" scope="external" format="https"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>以下是回應式影像位於採用網頁寬度50%的容器內的簡單範例。 每次調整瀏覽器視窗大小時，容器寬度就會變更。 當影像寬度達到配置的斷點之一時（為說明目的而設定為200、400、600和800像素），下載並顯示新的格式副本。 目的是避免載入不必要的大型影像，節省網路頻寬。 </p> <p>按一下URL以開啟網頁、調整瀏覽器視窗大小並監控網路流量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>以下Bootstrap範例說明網頁中的相同使用案例。 根據BootstrapCSS，新增回應式影像的版面儲存格會取得下列其中一個寬度：360、720和940像素。 這些值正是作為中斷點傳遞至回應式影像庫的內容。 因此，Dynamic Media可確保有效使用用戶端的網路頻寬。 此外，它還可確保影像以目前網頁版面所需的確切大小顯示，而不會因縮放用戶端瀏覽器而產生任何視覺成品。 </p> <p>按一下URL以開啟網頁、調整瀏覽器視窗大小以達到不同的版面中斷點，以及監控網路流量。 </p> <p>更高級的使用案例包括將不同的影像預設集或影像伺服命令（或兩者）與不同的斷點值相關聯。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>在下一個示例中，使用不同影像質量和格式的影像預設集（針對不同的斷點大小）。 對於小斷點，應用低質量預設，強制「影像服務」返回僅壓縮為六色的GIF影像。 媒體斷點正在使用為高壓縮的JPEG配置的影像預設集。 最大斷點與使用無損PNG的高質量影像預設集相關聯。 這種方法基於具有較大螢幕的設備具有更大的頻寬和處理能力的假設，確保將高質量影像傳送到這些設備。 </p> <p>按一下URL以開啟網頁，將網頁瀏覽器視窗的大小從大到小調整，並注意影像品質下降的情形。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>除了「影像預設集」之外，還可以將特定「影像伺服」命令與斷點關聯。 下列範例說明當螢幕影像大小變小時，如何將橫幅影像逐步裁切至感興趣的區域。 在此處，最大的斷點完全沒有任何「影像伺服」命令，因此橫幅影像是完全可見的。 在中斷點處應用適中裁切，使只能顯示文本為「正在運行」的運行器。 在小斷點處，應用更多的裁切，以便只顯示產品。 </p> <p>按一下URL以開啟網頁並調整瀏覽器視窗的大小。 注意影像在從大到小時會如何逐漸裁切。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>您也可以使用「影像伺服」命令搭配「影像伺服範本」，根據影像大小控制特定範本參數。 在下一個範例中，使用「影像提供範本」，其中文字覆蓋的字型大小是使用<span class="codeph"> $fontsize </span>參數參數化的。 回應式影像的設定是針對較小的影像大小使用較大的字型大小，以確保文字一律可讀： </p> </td> 
  </tr> 
 </tbody> 
</table>

## 系統需求 {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**伺服器硬體和軟體**

* Dynamic Media Image Serving 6.0.1或更新版本。

**用戶端瀏覽器最低需求**

* Microsoft® Windows® 7或更高版本；macOS X 10.8或更新版本。
* Firefox 23、Safari 6、Chrome 29、IE 9或更新版本。
* iOS 6或更新版本。
* 經iPhone3GS或更新版本以及iPad2或更新版本認證（僅限原生瀏覽器）。
* Android™ OS 2.3或更新版本。
* 目前不支援行動裝置上的Internet Explorer。
